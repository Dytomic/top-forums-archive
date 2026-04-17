# Banish Soul

**Category:** Source Development
**URL:** https://pkodev.com/threads/banish-soul.160/
**Posts:** 5

---

## Original Post
**Author:** zLuke  
**Date:** 2026-03-26

Banish Soul​[](#-banish-soul)Allows you to send a dead character to a save point.


---

### Reply #1
**Lullz** — 2026-03-26

you're a legend [@zLuke](https://pkodev.com/members/81/) !


---

### Reply #2
**ikaro** — 2026-04-10

god job lmao ![:geek:](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f913.png)


---

### Reply #3
**Lullz** — 2026-04-10

Suggested improvement:

When a player dies, give them a short protection time of 5-10 seconds. During this time, the ability "Banish Soul" cannot be used on them.

This change will prevent instant use of "Banish Soul" and give teammates time to revive the player.

You can also add a visual effect to the dead player during the protection time.


---

### Reply #4
**ikaro** — 2026-04-16

yo mate, checked out ur on-site revive code (for the third time hahaha) n welp, sick work!

just noticed a tiny UI quirk tho: when u die w/o the item in ur inv, the 'Resurrect' button & slot still show up greyed out, leaving the town button stuck awkwardly on the left side of the screen.

i tweaked CStartMgr::MainChaDied() a bit so it fully hides the resurrect UI when u dont have the item and auto-centers the town button, looks way cleaner imo.

heres the snippet if u wanna grab it and update the forum thread:

	
		C++:
	
	
	
		
```
 static CLabel* labReSpot = dynamic_cast<CLabel*>(frmMainChaRelive->Find("labReSpot"));
 static CImage* imgResurrectItem = dynamic_cast<CImage*>(frmMainChaRelive->Find("imgResurrectItem"));
 
 static CTextButton* pBtnReCity = dynamic_cast<CTextButton*>(frmMainChaRelive->Find("btnReCity"));
 static CLabel* labReCity = dynamic_cast<CLabel*>(frmMainChaRelive->Find("labReCity"));

 if (bHasItem && pBtnReSpot)
 {
 pBtnReSpot->SetIsShow(true);
 if (labReSpot) labReSpot->SetIsShow(true);
 if (imgResurrectItem) imgResurrectItem->SetIsShow(true);
 
 if (pBtnReCity) pBtnReCity->SetPos(34, 78);
 if (labReCity) labReCity->SetPos(34, 34);

 g_dwResurrectCountdownStartTime = CGameApp::GetCurTick();
 pBtnReSpot->SetIsEnabled(false); char szCaption[64];
 sprintf(szCaption, "%d", RESURRECT_COUNTDOWN_SECONDS);
 if (labReSpot) labReSpot->SetCaption(szCaption);
 }
 else if (pBtnReSpot)
 {
 pBtnReSpot->SetIsShow(false);
 if (labReSpot) labReSpot->SetIsShow(false);
 if (imgResurrectItem) imgResurrectItem->SetIsShow(false);

 if (pBtnReCity) pBtnReCity->SetPos(72, 78);
 if (labReCity) labReCity->SetPos(72, 34);

 pBtnReSpot->SetIsEnabled(false);
 if (labReSpot) labReSpot->SetCaption("Resurrect");
 g_dwResurrectCountdownStartTime = 0;
 }
```
