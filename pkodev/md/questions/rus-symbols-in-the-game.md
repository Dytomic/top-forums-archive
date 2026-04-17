# RUS symbols in the game?

**URL:** https://pkodev.com/threads/rus-symbols-in-the-game.154/
**Posts:** 6

---

## Original Post
**Author:** [TwT]~Darkness  
**Date:** 2026-03-21

Good afternoon. I’ve run into an issue with fonts in the game. The plan was to keep English as the main language, but add Russian text using “\” and generally implement Cyrillic characters in the game. However, everything ends up looking broken—the client refuses to display the font correctly.

Has anyone encountered something like this before? Could someone suggest how to fix it? My Windows settings are configured correctly, and UTF-8 is disabled. I set the server/client file encoding to ANSI, convert to ANSI, and then save. The characters do appear, but as you can see from the screenshots, they’re distorted.

Maybe someone can explain what’s going wrong?

Perhaps I made a mistake somewhere or missed something.

Thanks in advance to anyone who responds.

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
			
		![1774050946777.webp](https://pkodev.com/attachments/1774050946777-webp.324/)
		![1774051309799.webp](https://pkodev.com/attachments/1774051309799-webp.325/)
		![1774051371683.webp](https://pkodev.com/attachments/1774051371683-webp.326/)


---

### Reply #1
**zLuke** — 2026-03-21

This is a very ancient and lost knowledge.

In the MPFont.cpp file, remove all constructs of the following form:

	
		C++:
	
	
	
		
```
if ( *ch & 0x80 )
{
 ch++;
 offset = w * 2 + ASSIZE;
}
....
if ( ch[0] & 0x80 )
{
 n++;
 ch[1] = szText[n];
 offset = w + ASSIZE;
}
```


---

### Reply #2
**[TwT]~Darkness** — 2026-03-21

Wow ![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f929.png) lost knowledge, but you …. Your mind like library? ![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f607.png)![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f929.png)![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f607.png) thanks god ! This forum still have people like you! ![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f5a4.png) I’ll try.


---

### Reply #3
**[TwT]~Darkness** — 2026-03-24

> 
	
		
			
				[zLuke said:](/goto/post?id=404)
			
		
	
	
		
		
		
			This is a very ancient and lost knowledge.

In the MPFont.cpp file, remove all constructs of the following form:

	
		C++:
	
	
	
		
```
if ( *ch & 0x80 )
{
 ch++;
 offset = w * 2 + ASSIZE;
}
....
if ( ch[0] & 0x80 )
{
 n++;
 ch[1] = szText[n];
 offset = w + ASSIZE;
}
```


---

### Reply #4
**[TwT]~Darkness** — 2026-03-24

![1774323437939.webp](https://pkodev.com/attachments/1774323437939-webp.340/)

You are MY HERO! <3 

BUT!

We also need to change here

C++

LogFont.lfCharSet = RUSSIAN_CHARSET;

in this case u can typing in the game by russian + NPC show ur text on rus. BUT.... Still need to some fix. right now ill try. Here ill show my trying step by steb for everybody and also for my memories


---

### Reply #5
**[TwT]~Darkness** — 2026-03-24

zLuke​[](#-zluke)May God grant this man long life and prosperity! Both in his own project and in life! If it weren't for him, I'd still be digging around in C++, in files like:

::TextOutA( _hDc, 0, -2, sz, 1 );

::GetTextExtentPoint32A(_hDc, &ch[0], 1, &size);
CMPFont:![:D](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f600.png)rawText

And more else and else...
but thanks to the knowledge of this wonderful man, everything fell into place.
the last thing we do is go into:

scripts\lua\font.clu 

		![1774336186499.webp](https://pkodev.com/attachments/1774336186499-webp.343/)

We simply change these values (for starters), and that's it. The Russian language appears in the game in its original, excellent form!

***LOOK ^.^

		![1774336370258.webp](https://pkodev.com/attachments/1774336370258-webp.344/)***
​
