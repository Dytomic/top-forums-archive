# Glow bug on character position

**Category:** Client Help
**URL:** https://pkodev.com/threads/glow-bug-on-character-position.24/
**Posts:** 2

---

## Original Post
**Author:** Jesstef  
**Date:** 2026-01-25

Has anyone ever had this issue? I was trying to work with the bins (specificly sceneffect, but could it be related to it being messed up? or is it relevant for other files?

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
			
		![1769293104578.webp](https://pkodev.com/attachments/1769293104578-webp.1/)


---

### Reply #1
**Pixel** — 2026-01-27

Test this out:

Iteminfo.txt

8137 Aura Effect #37 n0072 10130005 0 0 0 0 0 0 44 0 0 0 0 0 1 1 1 1 1 0 60000 -1,-2,-2,-2 0 -1,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2 0 0 25 -1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0 0,0 25000,25000 0 0 0 0 0 0 0 0 0 0 0 0,0,0,0,0,0,0,0 0,0,0,0,0,0,0,0 583,-1 0,0 0,0 Put to glow app slot to obtain unique effect. 1

sceneeffectinfo.txt

583 lianhua.par 95bb?????? Sea Wave 0 0 -1 -1 0 1 0 -1
