# Shadow Font

**URL:** https://pkodev.com/threads/shadow-font.134/
**Posts:** 3

---

## Original Post
**Author:** ZkaRu  
**Date:** 2026-02-19

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
			
		![1771514046495.webp](https://pkodev.com/attachments/1771514046495-webp.117/)

I saw alot of ppl asking for this font, this isnt a specific font, u can modify it at UIHeadSay.cpp -> void CHeadSay::Render( D3DXVECTOR3& pos ) -> look for this "CGuiFont::s_Font.BRender(s_sNamePart*, x + iStartPosX, y - iNameHeightStep, s_dwNamePartsColors*[0], s_dwNamePartsColors*[1]);" and replace with:

int px = x + iStartPosX;

int py = y - iNameHeightStep;

DWORD textColor = s_dwNamePartsColors*[0];

DWORD outline = 0xFF000000; // black (u can change it)

for (int ox = -2; ox <= 2; ox++)

{

 for (int oy = -2; oy <= 2; oy++)

 {

 if (ox == 0 && oy == 0) continue;

 CGuiFont::s_Font.Render(s_sNamePart*, px + ox, py + oy, outline);

 }

}

CGuiFont::s_Font.Render(s_sNamePart*, px, py, textColor);

and thats it, u can change font too, at scripts->lua->font.clu******


---

### Reply #1
**zLuke** — 2026-02-20

Great, thanks for sharing. I did it a little differently.

MPFont.h

	
		C++:
	
	
	
		
```
bool DrawTextOutline(char* szText, int x, int y, D3DXCOLOR textColor, D3DXCOLOR outlineColor, int outlineWidth);
```


---

### Reply #2
**Mothanna** — 2026-02-21

you have to use some caches system fps will drop asf if many players appear on your scenes
