# Create a Quest

**Category:** Server Guides
**URL:** https://pkodev.com/threads/create-a-quest.147/
**Posts:** 4

---

## Original Post
**Author:** zLuke  
**Date:** 2026-03-06

This guide was copied from the website [https;//pkodev.net](http://https;//pkodev.net), by the author Angelix​[](#-this-guide-was-copied-from-the-website-https-pkodev-net-by-the-author-angelix)
**Simple Quest Part I**

Collect an item, able to repeat after finishing.​

**[Spoiler: Click to expand]**

		
		
			Adding a small format that will be explained below.

	
		HTML:
	
	
	
		
```
 DefineMission(<QUEST_ID>, <QUEST_NAME>, <MISSION_ID>)

 MisBeginTalk(<MAIN_DIALOG>)

 MisBeginCondition(NoMission, <MISSION_ID>)
 MisBeginAction(AddMission, <MISSION_ID>)
 MisBeginAction(AddTrigger, <TRIGGERID>, TE_GETITEM, <ITEMINFO_ID>, <AMOUNT_NEEDED>)
 MisCancelAction(ClearMission, <MISSION_ID>)

 MisNeed(MIS_NEED_ITEM, <ITEMINFO_ID>, <AMOUNT_NEEDED>, <MISSION_FLAG>, <AMOUNT_NEEDED>)

 MisResultTalk(<COMPLETION_DIALOG>)

 MisHelpTalk(<HELP_DIALOG>)

 MisResultCondition(HasMission, <MISSION_ID>)
 MisResultCondition(HasItem, <ITEMINFO_ID>, <AMOUNT_NEEDED>)
 MisResultAction(TakeItem, <ITEMINFO_ID>, <AMOUNT_NEEDED>)
 MisResultAction(ClearMission, <MISSION_ID>)

 InitTrigger()
 TriggerCondition(1, IsItem, <ITEMINFO_ID>)
 TriggerAction(1, AddNextFlag, <MISSION_ID>, <MISSION_FLAG>, <AMOUNT_NEEDED>)
 RegCurTrigger(<TRIGGERID>)
```


---

### Reply #1
**zLuke** — 2026-03-06

**Custom Quest Part I**

Making the players kill other players within the quest.​

**[Spoiler: Click to expand]**

		
		
			In this part of the guide, I'll be showing you how to add a little trick to make quest that ask for killing players. It's a bit more complicated since you'll have to edit an already existing function, add a new function and a new line within CharacterInfo. You'll be following the same structure from ***Simple Quest Part II***, I'll just show what to modify and add.

Lets start by adding a new line within CharacterInfo:

	
		HTML:
	
	
	
		
```
<CHARACTERINFO_ID> <CHARACTER_NAME> Long Haired Guy 1 1 0 0 100 2000 255 464 640 816 0 0 0 0,0 0 0,0,0 1 1 100 182 -1 -1 0 0 0 1,2,3,4,7,8 1.051 1.369 2.599 40 1,5 0,0 399 398 0 0 0,0,0 1 1 0 0 25,28,29,30,31,34,35,38 100 0 0 0 0 0 0 0 1 1 1000 0 0 1 0 1 40 0 18 0 4 5 0 3 2 1 1 0 1 1 1442 0 1500 480 0 5 5 5 5 5 5 20 0 0 0 0 20 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1.0,1.0,1.0
```


---

### Reply #2
**zLuke** — 2026-03-06

**Extra Quest Functions Part I**

Adding rewards to quests.​

**[Spoiler: Click to expand]**

		
		
			Taking a look at the format from "Simple Quest Part I", you can add some functions to give players items, gold or do other actions.

After this line:

	
		HTML:
	
	
	
		
```
MisResultAction(ClearMission, <MISSION_ID>)
```


---

### Reply #3
**zLuke** — 2026-03-06

Programs for creating quests.
