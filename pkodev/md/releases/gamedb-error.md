# GAMEDB ERROR

**URL:** https://pkodev.com/threads/gamedb-error.137/
**Posts:** 10

---

## Original Post
**Author:** iamkennd  
**Date:** 2026-02-21

Hello, good morning, afternoon/night to everyone!!

I'm getting some problem to connect database, and the only problem is GameServer.

I can open all exes (Accountserver, GateServer, GroupServer) but i can't GameServer cuz it gives me error

as you can see, all the exes is working perfectly, except GameServer.

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
			
		![1771687711681.webp](https://pkodev.com/attachments/1771687711681-webp.232/)

So thats configuration:

GAMESERVER

		![1771687765751.webp](https://pkodev.com/attachments/1771687765751-webp.233/)

ACCOUNTSERVER

		![1771687786604.webp](https://pkodev.com/attachments/1771687786604-webp.234/)

GROUPSERVER

		![1771687808944.webp](https://pkodev.com/attachments/1771687808944-webp.235/)

i'm Using SQL 2018 version, and thats my configuration:

		![1771687888069.webp](https://pkodev.com/attachments/1771687888069-webp.236/)
		![1771687905428.webp](https://pkodev.com/attachments/1771687905428-webp.237/)

Thats it.

If someone can help me i'll be gratefull! Thank you <3


---

### Reply #1
**ZkaRu** — 2026-02-21

add username and pass


---

### Reply #2
**iamkennd** — 2026-02-21

> 
	
		
			
				[ZkaRu said:](/goto/post?id=304)
			
		
	
	
		
		
		
			add username and pass
		
		
		Click to expand...


---

### Reply #3
**zLuke** — 2026-02-21

![1771692524813.webp](https://pkodev.com/attachments/1771692524813-webp.248/)
		![1771692557026.webp](https://pkodev.com/attachments/1771692557026-webp.249/)

		![1771692753048.webp](https://pkodev.com/attachments/1771692753048-webp.250/)

Check this.

Use login and password in config files, it's correct


---

### Reply #4
**iamkennd** — 2026-02-21

> 
	
		
			
				[zLuke said:](/goto/post?id=306)
			
		
	
	
		
		
		
			[View attachment 248](https://pkodev.com/attachments/248/)[View attachment 249](https://pkodev.com/attachments/249/)
[View attachment 250](https://pkodev.com/attachments/250/)

Check this.

Use login and password in config files, it's correct
		
		
		Click to expand...


---

### Reply #5
**iamkennd** — 2026-02-21

> 
	
		
			
				[zLuke said:](/goto/post?id=306)
			
		
	
	
		
		
		
			[View attachment 248](https://pkodev.com/attachments/248/)[View attachment 249](https://pkodev.com/attachments/249/)
[View attachment 250](https://pkodev.com/attachments/250/)

Check this.

Use login and password in config files, it's correct
		
		
		Click to expand...


---

### Reply #6
**Grim4ik** — 2026-02-21

> 
	
		
			
				[iamkennd said:](/goto/post?id=308)
			
		
	
	
		
		
		
			[View attachment 254](https://pkodev.com/attachments/254/)

Everything works fine with SQL and config files, but i got this error to connect the char to the game, any way to solve it?

[View attachment 256](https://pkodev.com/attachments/256/)
		
		
		Click to expand...


---

### Reply #7
**zLuke** — 2026-02-21

Download .obj files [https://github.com/mothannakhzaleh/TalesOfPirateDX9/tree/main/Client/map](https://github.com/mothannakhzaleh/TalesOfPirateDX9/tree/main/Client/map)

Or use files from another client.


---

### Reply #8
**iamkennd** — 2026-02-21

> 
	
		
			
				[zLuke said:](/goto/post?id=310)
			
		
	
	
		
		
		
			Download .obj files [https://github.com/mothannakhzaleh/TalesOfPirateDX9/tree/main/Client/map](https://github.com/mothannakhzaleh/TalesOfPirateDX9/tree/main/Client/map)

Or use files from another client.
		
		
		Click to expand...


---

### Reply #9
**iamkennd** — 2026-02-21

![1771696170417.webp](https://pkodev.com/attachments/1771696170417-webp.258/)

Works perfectly! Thanks to zLuke, monthanna and whole forum.
