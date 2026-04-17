# NPC characters\skills\points

**URL:** https://pkodev.com/threads/npc-characters-skills-points.155/
**Posts:** 6

---

## Original Post
**Author:** [TwT]~Darkness  
**Date:** 2026-03-21

Hello everybody!

I’m also trying to do the following:​

I’m trying to create an NPC that will grant character bonuses for completing a mission.

Could you check whether this function will work?

The last time I dealt with something like this (about 20 years ago), I had an issue with experience removal. The character would gain 1 level, but after gaining any experience in the game, the level would revert to what it was before turning in the quest.

Did I properly define the structure for saving what the NPC grants? Or maybe different commands are needed? Could they behave the same way as GM commands? For example, I can reward a player by ID with strength, HP, agility, or constitution. But after teleporting to another city or relogging, the character’s stats return to their original values.

Is there some kind of function to “permanently закрепить” (lock in / persist) the acquired bonuses so they stay with the character forever?

The quest is intended to be long-term.

So after each completion, depending on whether the player has a certain item and has completed it before, the reward bonus would increase.

What do you think?

function dream_talk28()

 Talk(1,"Bring me 5 required items, kill 6 monster groups, and pay 10000 gold. I will rebuild your character and give rewards.")

 InitTrigger()

 -- Если миссии нет, предложить взять

 TriggerCondition(1, NoMission, 9000)

 TriggerCondition(1, NoRecord, 9000)

 TriggerAction(1, AddMission, 9000)

 TriggerAction(1, ReAll)

 -- Если миссия уже есть, просто показать текст

 TriggerFailure(1, JumpPage, 2)

 Text(1,"I want to accept the mission.", MultiTrigger, GetMultiTrigger(), 1)

 Talk(2,"You already have this mission or have already completed it.")

end

function CustomResetReward(Player)

 --------------------------------------------------

 -- 1. СБРОС УРОВНЯ И ОПЫТА

 --------------------------------------------------

 SetChaAttr(Player, ATTR_LV, 1)

 SetChaAttr(Player, ATTR_CEXP, 0)

 --------------------------------------------------

 -- 2. СТАТЫ СТАВИМ ПО 10

 --------------------------------------------------

 SetChaAttr(Player, ATTR_STR, 10)

 SetChaAttr(Player, ATTR_DEX, 10)

 SetChaAttr(Player, ATTR_AGI, 10)

 SetChaAttr(Player, ATTR_CON, 10)

 SetChaAttr(Player, ATTR_STA, 10)

 --------------------------------------------------

 -- 3. СВОБОДНЫЕ ПОИНТЫ

 --------------------------------------------------

 SetChaAttr(Player, ATTR_AP, 10)

 --------------------------------------------------

 -- 4. ПОСТОЯННЫЕ БОНУСЫ

 --------------------------------------------------

 -- Max HP +10000?

 -- Или ATTR_MXHP?

 local cur_mxhp = GetChaAttr(Player, ATTR_MXHP)

 SetChaAttr(Player, ATTR_MXHP, cur_mxhp + 10000)

 -- DEF +100

 local cur_def = GetChaAttr(Player, ATTR_DEF)

 SetChaAttr(Player, ATTR_DEF, cur_def + 100)

 -- Move Speed +100

 local cur_mspd = GetChaAttr(Player, ATTR_MSPD)

 SetChaAttr(Player, ATTR_MSPD, cur_mspd + 100)

 --------------------------------------------------

 -- 5. ФЛАГ ДЛЯ СОХРАНЕНИЯ / ПРОВЕРКИ

 --------------------------------------------------

 -- Сохраняем бонусы ?

 -- можно проверять этот record?

 SetRecord(Player, 9100)

 --------------------------------------------------

 -- 6. ОБНОВЛЕНИЕ

 --------------------------------------------------

 SyncCha(Player)

 SystemNotice(Player, "Reset complete. Your character was rebuilt successfully.")

end


---

### Reply #1
**[TwT]~Darkness** — 2026-03-21

{
				"lightbox_close": "Close",
				"lightbox_next": "Next",
				"lightbox_previous": "Previous",
				"lightbox_error": "The requested content cannot be loaded. Please try again later.",
				"lightbox_start_slideshow": "Start slideshow",
				"lightbox_stop_slideshow": "Stop slideshow",
				"lightbox_full_screen": "Full screen",
				"lightbox_thumbnails": "Thumbnails",
				"lightbox_download": "Download",
				"lightbox_share": "Share",
				"lightbox_zoom": "Zoom",
				"lightbox_new_window": "New window",
				"lightbox_toggle_sidebar": "Toggle sidebar"
			}
			
		![1774052621253.webp](https://pkodev.com/attachments/1774052621253-webp.330/)

Looks like broken. I think cuz i have not full functional of this NPC, correct?

Also im forgot where i can change this function, IF!

BASED r_talk - diapered. i mean hasnt fucntion r_talk with this type of NPC im my files.

in this case - just creating new one? 

And where i can check drop + full function + % of drop inside this machine ?

Thanks.


---

### Reply #2
**zLuke** — 2026-03-21

Jackpot - file function.lua function TigerStart(...)


---

### Reply #3
**zLuke** — 2026-03-21

The calculation of character parameters depends on many factors, such as level, items, gems, stats, and skills. You can't just add +1000 HP to a character, and everything will be calculated based on that +1000 HP.

Do it differently. Create a piece of jewelry without stats, for example, and give it out as a quest reward. Then, as you complete the quest, add stats to the jewelry as a reward.


---

### Reply #4
**[TwT]~Darkness** — 2026-03-23

> 
	
		
			
				[zLuke said:](/goto/post?id=406)
			
		
	
	
		
		
		
			The calculation of character parameters depends on many factors, such as level, items, gems, stats, and skills. You can't just add +1000 HP to a character, and everything will be calculated based on that +1000 HP.

Do it differently. Create a piece of jewelry without stats, for example, and give it out as a quest reward. Then, as you complete the quest, add stats to the jewelry as a reward.
		
		
		Click to expand...


---

### Reply #5
**zLuke** — 2026-03-23

Unfortunately, adding stats using the GM command only works until the first teleport or relogin.
