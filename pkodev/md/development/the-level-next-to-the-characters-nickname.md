# The level next to the character’s nickname

**Category:** Source Development
**URL:** https://pkodev.com/threads/the-level-next-to-the-characters-nickname.122/
**Posts:** 2

---

## Original Post
**Author:** Grim4ik  
**Date:** 2026-01-29

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
			
		![image.png.745542f254250645f816e8d1ede6772b.webp](https://pkodev.com/attachments/image-png-745542f254250645f816e8d1ede6772b-webp.63/)

Open **UIHeadSay.cpp**

Find:

	
		C++:
	
	
	
		
```
 for (int i(0); i<NAME_PART_NUM; i++)
 {
 if( s_dwNamePartsColors[i][1] )
 {
 CGuiFont::s_Font.BRender(s_sNamePart[i], x + iStartPosX, y - iNameHeightStep, s_dwNamePartsColors[i][0], s_dwNamePartsColors[i][1] );
 }
 else
 {
 CGuiFont::s_Font.Render(s_sNamePart[i], x + iStartPosX, y - iNameHeightStep, s_dwNamePartsColors[i][0] );
 }
 iStartPosX += CGuiFont::s_Font.GetWidth(s_sNamePart[i]);
 }
```


---

### Reply #1
**lexbergeron** — 2026-01-30

Thank you ![:)](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f642.png)
