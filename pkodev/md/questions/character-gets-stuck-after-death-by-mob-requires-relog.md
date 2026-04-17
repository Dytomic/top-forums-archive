# Character Gets Stuck After Death by Mob (Requires Relog)

**Category:** Source Help
**URL:** https://pkodev.com/threads/character-gets-stuck-after-death-by-mob-requires-relog.161/
**Posts:** 11

---

## Original Post
**Author:** Grim4ik  
**Date:** 2026-03-28

Hello!

I’ve run into an issue and was wondering if anyone else has experienced this or knows how to fix it.

After dying to a mob, the player receives a system message like the one shown in the screenshot.

The character then becomes stuck in the world, and the player needs to relog. After relogging, the character respawns at their spawn point.

However, when dying to another player, everything works correctly — a resurrection notification appears as expected.


---

### Reply #1
**zLuke** — 2026-03-28

Check if you have translated the NPC scripts to another language, and the respawn point is recorded in the database in Russian (Аргент), but the respawn point in birth_conf.lua is in another language (Argent City), so the server cannot find the respawn point because it is looking for it by name in birth_conf.lua.


---

### Reply #2
**Grim4ik** — 2026-03-28

> 
	
		
			
				[zLuke said:](/goto/post?id=438)
			
		
	
	
		
		
		
			Check if you have translated the NPC scripts to another language, and the respawn point is recorded in the database in Russian (Аргент), but the respawn point in birth_conf.lua is in another language (Argent City), so the server cannot find the respawn point because it is looking for it by name in birth_conf.lua.
		
		
		Click to expand...


---

### Reply #3
**zLuke** — 2026-03-28

So when you die from a mob, you get a respawn window?


---

### Reply #4
**Grim4ik** — 2026-03-28

> 
	
		
			
				[zLuke said:](/goto/post?id=440)
			
		
	
	
		
		
		
			So when you die from a mob, you get a respawn window?
		
		
		Click to expand...


---

### Reply #5
**zLuke** — 2026-03-29

Цепочка вызовов.

В CFightAble::SkillTarEffect(SFireUnit*) при lOldHP>0 и lNowHP<=0: вызывается SetDie(pSrcCha)

▼

В CFightAble::SetDie(CCharacter* pCSkillSrcCha) если убийца игрок то идем в ветку lua DoString("after_player_kill_player")

если моб то JustDie(pCSkillSrcCha)

▼

В CCharacter::JustDie(pCSrcCha) вызывается g_EventHandler.Event_ChaDie(this, pCSrcCha)

▼

В CEventHandler::Event_ChaDie(pDead, pAtk) если убийца не игрок

CPlayer *pPlayer = pAtk->GetPlayer();

if(pPlayer==NULL)

идем в lua и по цепочке вызываем GetExp_New -> GetExp_MKP -> Dead_Punish

Как раз в Dead_Punish отображается строка в системе SystemNotice(dead, "Death penalty. EXP lost: " .. exp_red)

и вызывается Dead_Punish_ItemURE(dead) штраф на экипировку SystemNotice(role, "Death penalty: lost 5%% equipment durability")

▼

Возврат в CFightAble::SkillTarEffect(SFireUnit*) и вызов NotiSkillTarToEyeshot(pSFireSrc)

▼

В CFightAble::NotiSkillTarToEyeshot(SFireUnit *pSFireSrc) отправляем пакет CMD_MC_NOTIACTION клиенту с уведомлением всех персонажей (и себе тоже) в области видимости с полями

WRITE_LONG(pk, m_ID); ID трупа

WRITE_SHORT(pk, m_SFightProc.sState); статус ( должен быть enumFSTATE_DIE) устанавливается в SkillTarEffect

Клиент.

Сеть → CMD_MC_NOTIACTION

▼

SC_CharacterAction (PacketCmd_SC.cpp)

▼

case enumACTION_SKILL_TAR: разбор полей → NetActorSkillEff (NetProtocol.cpp)

▼

если SkillEff.sState & enumFSTATE_DIE и цель — главный персонаж:

 CAttackEffect::ChaDied(pTarget, pAttack) (HMAttack.cpp)

▼

CReadyDieState::_Start (STReadyDie.cpp)

▼

CStartMgr::MainChaDied (UIStartForm.cpp)

▼

frmMainChaRelive->Show() — форма "frmRelive" из UI

Добавь в начало CFightAble::NotiSkillTarToEyeshot

	
		C++:
	
	
	
		
```
LG("NotiSkillTar",
 "NotiSkillTarToEyeshot tar=%s id=%u sState=0x%04X (%d) skillId=%d srcId=%u\n",
 IsCharacter()->GetLogName(),
 m_ID,
 (unsigned)(unsigned short)m_SFightProc.sState,
 (int)m_SFightProc.sState,
 pSFireSrc->pCSkillRecord ? (int)pSFireSrc->pCSkillRecord->sID : -1,
 pSFireSrc->ulID);
```


---

### Reply #6
**Grim4ik** — 2026-03-29

> 
	
		
			
				[zLuke said:](/goto/post?id=442)
			
		
	
	
		
		
		
			Цепочка вызовов.

В CFightAble::SkillTarEffect(SFireUnit*) при lOldHP>0 и lNowHP<=0: вызывается SetDie(pSrcCha)

▼

В CFightAble::SetDie(CCharacter* pCSkillSrcCha) если убийца игрок то идем в ветку lua DoString("after_player_kill_player")

если моб то JustDie(pCSkillSrcCha)

▼

В CCharacter::JustDie(pCSrcCha) вызывается g_EventHandler.Event_ChaDie(this, pCSrcCha)

▼

В CEventHandler::Event_ChaDie(pDead, pAtk) если убийца не игрок

CPlayer *pPlayer = pAtk->GetPlayer();

if(pPlayer==NULL)

идем в lua и по цепочке вызываем GetExp_New -> GetExp_MKP -> Dead_Punish

Как раз в Dead_Punish отображается строка в системе SystemNotice(dead, "Death penalty. EXP lost: " .. exp_red)

и вызывается Dead_Punish_ItemURE(dead) штраф на экипировку SystemNotice(role, "Death penalty: lost 5%% equipment durability")

▼

Возврат в CFightAble::SkillTarEffect(SFireUnit*) и вызов NotiSkillTarToEyeshot(pSFireSrc)

▼

В CFightAble::NotiSkillTarToEyeshot(SFireUnit *pSFireSrc) отправляем пакет CMD_MC_NOTIACTION клиенту с уведомлением всех персонажей (и себе тоже) в области видимости с полями

WRITE_LONG(pk, m_ID); ID трупа

WRITE_SHORT(pk, m_SFightProc.sState); статус ( должен быть enumFSTATE_DIE) устанавливается в SkillTarEffect

Клиент.

Сеть → CMD_MC_NOTIACTION

▼

SC_CharacterAction (PacketCmd_SC.cpp)

▼

case enumACTION_SKILL_TAR: разбор полей → NetActorSkillEff (NetProtocol.cpp)

▼

если SkillEff.sState & enumFSTATE_DIE и цель — главный персонаж:

 CAttackEffect::ChaDied(pTarget, pAttack) (HMAttack.cpp)

▼

CReadyDieState::_Start (STReadyDie.cpp)

▼

CStartMgr::MainChaDied (UIStartForm.cpp)

▼

frmMainChaRelive->Show() — форма "frmRelive" из UI

Добавь в начало CFightAble::NotiSkillTarToEyeshot

	
		C++:
	
	
	
		
```
LG("NotiSkillTar",
 "NotiSkillTarToEyeshot tar=%s id=%u sState=0x%04X (%d) skillId=%d srcId=%u\n",
 IsCharacter()->GetLogName(),
 m_ID,
 (unsigned)(unsigned short)m_SFightProc.sState,
 (int)m_SFightProc.sState,
 pSFireSrc->pCSkillRecord ? (int)pSFireSrc->pCSkillRecord->sID : -1,
 pSFireSrc->ulID);
```


---

### Reply #7
**zLuke** — 2026-03-29

Смотри функцию

	
		C++:
	
	
	
		
```
void CFightAble::SetDie(CCharacter *pCSkillSrcCha)
{
 SetItemHostObj(0);
 SetExistState(enumEXISTS_WITHERING);
 m_SFightInit.chTarType = 0;
 m_SFightProc.sState = enumFSTATE_DIE;
 m_SExistCtrl.ulTick = GetTickCount();
 RemoveAllSkillState();
 m_CSkillState.Reset();

 CCharacter *pCDieCha = this->IsCharacter();
 if (pCSkillSrcCha && pCSkillSrcCha != g_pCSystemCha)
 {
 pCDieCha->JustDie(pCSkillSrcCha);
 }

 pCDieCha->m_pHate->ClearHarmRec();

 if (pCDieCha->IsPlayerOwnCha() && pCSkillSrcCha && pCSkillSrcCha->IsPlayerOwnCha())
 {
 g_CParser.DoString("after_player_kill_player", enumSCRIPT_RETURN_NONE, 0, enumSCRIPT_PARAM_LIGHTUSERDATA, 2, pCSkillSrcCha, pCDieCha, DOSTRING_PARAM_END);
 }
}
```


---

### Reply #8
**Grim4ik** — 2026-03-29

> 
	
		
			
				[zLuke said:](/goto/post?id=447)
			
		
	
	
		
		
		
			Смотри функцию

	
		C++:
	
	
	
		
```
void CFightAble::SetDie(CCharacter *pCSkillSrcCha)
{
 SetItemHostObj(0);
 SetExistState(enumEXISTS_WITHERING);
 m_SFightInit.chTarType = 0;
 m_SFightProc.sState = enumFSTATE_DIE;
 m_SExistCtrl.ulTick = GetTickCount();
 RemoveAllSkillState();
 m_CSkillState.Reset();

 CCharacter *pCDieCha = this->IsCharacter();
 if (pCSkillSrcCha && pCSkillSrcCha != g_pCSystemCha)
 {
 pCDieCha->JustDie(pCSkillSrcCha);
 }

 pCDieCha->m_pHate->ClearHarmRec();

 if (pCDieCha->IsPlayerOwnCha() && pCSkillSrcCha && pCSkillSrcCha->IsPlayerOwnCha())
 {
 g_CParser.DoString("after_player_kill_player", enumSCRIPT_RETURN_NONE, 0, enumSCRIPT_PARAM_LIGHTUSERDATA, 2, pCSkillSrcCha, pCDieCha, DOSTRING_PARAM_END);
 }
}
```


---

### Reply #9
**zLuke** — 2026-03-29

То есть в SetDie устанавливается m_SFightProc.sState= enumFSTATE_DIE;

И тут же в лог пишется sState=0x0010 (16)? 

Очень странно.


---

### Reply #10
**Grim4ik** — 2026-03-31

I would like to express my sincere gratitude to [@zLuke](https://pkodev.com/members/81/), who helped identify the problem.

The issue turned out to be in one of my Lua features.
