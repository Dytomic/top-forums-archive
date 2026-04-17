# Tales of Pirate 2026 DX9 by alexxst.st

**Category:** Source
**URL:** https://pkodev.com/threads/tales-of-pirate-2026-dx9-by-alexxst-st.162/
**Posts:** 13

---

## Original Post
**Author:** alexxst  
**Date:** 2026-03-30

Hi

I'm presenting my version of Pirate King Online (PKO), which will be actively developed with ongoing bug fixes.

		
			
				
					
						![github.com](https://opengraph.githubassets.com/8ff835edf5e09f4b20fd819de7f43e2e6d3013471fa74254a24652e1aa801381/alexxstst/TalesOfPirate)
			
			
				
					[
						GitHub - alexxstst/TalesOfPirate at draft
					]()
				

				this repository contain tales of pirate source as 2022, and upraded to dx 9 - alexxstst/TalesOfPirate

				
					
						
							![github.com](https://github.githubassets.com/favicons/favicon.svg)
					github.com


---

### Reply #1
**astrobomb** — 2026-03-31

These Mothana files have an FPS issue due to improper application of DirectX 9. I tested them for 3 months.


---

### Reply #2
**alexxst** — 2026-03-31

> 
	
		
			
				[astrobomb said:](/goto/post?id=452)
			
		
	
	
		
		
		
			These Mothana files have an FPS issue due to improper application of DirectX 9. I tested them for 3 months.
		
		
		Click to expand...


---

### Reply #3
**astrobomb** — 2026-03-31

I can send you the complete error report for those files. Send me your Discord.


---

### Reply #4
**alexxst** — 2026-03-31

Only github for errors & bugs. There are file attachment mechanisms there.


---

### Reply #5
**Mothanna** — 2026-03-31

not bad , have u tested new exes fo login etc?

we did few tools for login, and test same as bareclient kind good way to test current exe same when people play,login,talk etc

, people sit and complain about fps while they create the bug it wasn't even exist ingame

they force name show, etc and it use "Draw" in very bad way to consuming gpu but since all their games using cpu , so u can image how suck its going

this small example how same source can be very different if you use correct methods of renders 
[example as video](https://cdn.discordapp.com/attachments/1482808729706430697/1483081460377190400/20260316-1235-51.2369600.mp4?ex=69cd113e&is=69cbbfbe&hm=a53f897e4c7b70207c1de493771c88fcc2d579efe01d4a9f1c50aa74129b2e48&)

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
			
		![1774973081098.webp](https://pkodev.com/attachments/1774973081098-webp.362/)


---

### Reply #6
**alexxst** — 2026-03-31

From a security point of view, it's better.

Not yet, I'm currently focused on the task of organizing the game's resources - putting all the txt files in one place, sqlite, so that they can be edited without errors by any DB client. This has accelerated the client's loading by a factor of 4.

Then I'll focus on the resources - models and images. I'll create a more stable system for loading them into the client.

I'll update SDL

And I'll convert everything to x64

And then I'll work on the engine and try to squeeze everything out of it.


---

### Reply #7
**siegi** — 2026-04-02

can i use

> 
	
		
			
				[alexxst said:](/goto/post?id=455)
			
		
	
	
		
		
		
			I would say it's not just one problem, but I've counted more than 5... The frame rate is incorrect, and it needs to be fixed. My main goal is to bring the client to a more stable state, where resources load properly, there are no crashes, and errors are easily diagnosable. I will definitely fix the FPS this week or next. You can create an ISSUE [https://github.com/alexxstst/TalesOfPirate/issues](https://github.com/alexxstst/TalesOfPirate/issues) on GitHub to remind me to fix it.
		
		
		Click to expand...


---

### Reply #8
**alexxst** — 2026-04-02

> 
	
		
			
				[siegi said:](/goto/post?id=464)
			
		
	
	
		
		
		
			can i use

Can i use Xampp Mysql to connect databases or i need another mysql?
		
		
		Click to expand...


---

### Reply #9
**alexxst** — 2026-04-04

After switching to sqlite, the server and client loading time in debug mode has significantly decreased. If you add SQLCipher instead of SQLite, you will get protected resources using AES-256 in one place.

 I have converted the MindPower3D engine into a static C++ library, which has fixed several bugs at once - static variables declared in shared modules periodically overlap each other and serve as a generator of data duplication.

 Now I plan to pack localization into sqlite to finally get rid of all the garbage files and ICU.

 And make a full-fledged release in master that only needs to be launched.

P.S. The resource file that I attached can be opened by any program for database. For example, DBeaver. It is much easier to edit it than text files

	
		Code:
	
	
	
		
```
Debug |common| GameRecordset<class CShadeInfo> loaded 7 records in 0 ms (id range: 1..7)
Debug |common| GameRecordset<class CEventSoundInfo> loaded 4 records in 0 ms (id range: 1..4)
Debug |common| GameRecordset<class CMusicInfo> loaded 394 records in 1 ms (id range: 1..456)
Debug |common| GameRecordset<class CPoseInfo> loaded 54 records in 0 ms (id range: 1..54)
Debug |common| GameRecordset<class CChaCreateInfo> loaded 4 records in 0 ms (id range: 1..4)
Debug |common| GameRecordset<class CMapInfo> loaded 41 records in 0 ms (id range: 1..49)
Debug |common| GameRecordset<class CEventRecord> loaded 4 records in 0 ms (id range: 1..4)
Debug |common| GameRecordset<class CServerGroupInfo> loaded 2 records in 0 ms (id range: 1..2)
Debug |common| GameRecordset<class CItemRecord> loaded 6337 records in 692 ms (id range: 1..32767)
Debug |common| GameRecordset<class CAreaInfo> loaded 255 records in 2 ms (id range: 1..255)
Debug |common| GameRecordset<class CNotifyInfo> loaded 2 records in 0 ms (id range: 1..2)
Debug |common| GameRecordset<class CChatIconInfo> loaded 8 records in 0 ms (id range: 1..8)
Debug |common| GameRecordset<class CItemTypeInfo> loaded 38 records in 0 ms (id range: 1..64)
Debug |common| GameRecordset<class CItemPreInfo> loaded 100 records in 0 ms (id range: 0..99)
Debug |common| GameRecordset<class EFF_Param> loaded 53 records in 0 ms (id range: 10..62)
Debug |common| GameRecordset<class Group_Param> loaded 4 records in 0 ms (id range: 1..4)
Debug |common| GameRecordset<class CItemRefineInfo> loaded 236 records in 3 ms (id range: 4..6091)
Debug |common| GameRecordset<class CItemRefineEffectInfo> loaded 112 records in 1 ms (id range: 1..200)
Debug |common| GameRecordset<class CForgeRecord> loaded 12 records in 0 ms (id range: 1..12)
Debug |common| GameRecordset<struct xShipInfo> loaded 17 records in 0 ms (id range: 1..17)
Debug |common| GameRecordset<struct xShipPartInfo> loaded 212 records in 1 ms (id range: 1..212)
Debug |common| GameRecordset<class CChaRecord> loaded 1650 records in 158 ms (id range: 1..1650)
Debug |common| GameRecordset<class CSkillRecord> loaded 411 records in 33 ms (id range: 1..475)
Debug |common| GameRecordset<class CSkillStateRecord> loaded 194 records in 3 ms (id range: 1..221)
Debug |common| GameRecordset<class CHairRecord> loaded 210 records in 3 ms (id range: 1..210)
Debug |common| GameRecordset<class MPTerrainInfo> loaded 49 records in 0 ms (id range: 1..49)
Debug |common| GameRecordset<class CSceneObjInfo> loaded 1202 records in 21 ms (id range: 1..1292)
Debug |common| GameRecordset<class CMagicInfo> loaded 1093 records in 7 ms (id range: 1..4087)
Debug |common| GameRecordset<class NPCData> loaded 354 records in 1 ms (id range: 0..353)
Debug |common| GameRecordset<class NPCData> loaded 348 records in 1 ms (id range: 1..348)
Debug |common| GameRecordset<class CMonsterInfo> loaded 585 records in 4 ms (id range: 1..585)
Debug |common| GameRecordset<class CMountInfo> loaded 20 records in 0 ms (id range: 1..20)
Debug |common| GameRecordset<class CResourceInfo> loaded 6 records in 0 ms (id range: 1..7)
Debug |common| GameRecordset<class CStoneInfo> loaded 44 records in 0 ms (id range: 1..53)
Debug |common| GameRecordset<class CElfSkillInfo> loaded 27 records in 0 ms (id range: 1..27)
Debug |common| GameRecordset<class CHelpInfo> loaded 0 records in 0 ms (id range: 0..0)
```


---

### Reply #10
**fernando.andrade98@gmail.** — 2026-04-05

I'm so bad with these files that I couldn't even open them to test them. How can I run this?


---

### Reply #11
**[TwT]~Darkness** — 2026-04-06

> 
	
		
			
				[fernando.andrade98@gmail. said:](/goto/post?id=473)
			
		
	
	
		
		
		
			Я настолько плохо разбираюсь в этих файлах, что даже не смог открыть их для тестирования. Как мне это запустить?
		
		
		Click to expand...


---

### Reply #12
**dragontechi** — 2026-04-07

[@alexxst](https://pkodev.com/members/201/) 

> 
	
		
			
				[alexxst said:](/goto/post?id=451)
			
		
	
	
		
		
		
			Hi

I'm presenting my version of Pirate King Online (PKO), which will be actively developed with ongoing bug fixes.

		
			
				
					
						![github.com](https://opengraph.githubassets.com/8ff835edf5e09f4b20fd819de7f43e2e6d3013471fa74254a24652e1aa801381/alexxstst/TalesOfPirate)
			
			
				
					[
						GitHub - alexxstst/TalesOfPirate at draft
					]()
				

				this repository contain tales of pirate source as 2022, and upraded to dx 9 - alexxstst/TalesOfPirate

				
					
						
							![github.com](https://github.githubassets.com/favicons/favicon.svg)
					github.com
