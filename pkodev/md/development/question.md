# Question?

**URL:** https://pkodev.com/threads/question.167/
**Posts:** 2

---

## Original Post
**Author:** fernando.andrade98@gmail.  
**Date:** 2026-04-11

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
			
		![1775873712583.webp](https://pkodev.com/attachments/1775873712583-webp.399/)

Hello my friends, how are you?

I'm using the server provided by our team, the best of the best, for testing.

Well, I'm learning a few things:

1. First, the password is set to an old pattern, BLAKE2s?

2. Second, I added the import code but it doesn't appear in the marketplace, why?


---

### Reply #1
**zLuke** — 2026-04-11

1.1 You can revert to using the old md5 option [https://pkodev.com/threads/website-for-tales-of-pirate-2022-dx9.146/post-444](https://pkodev.com/threads/website-for-tales-of-pirate-2022-dx9.146/post-444)

1.2 Implement BLAKE2s in your WEB binding. Starting from version 7.1, php supports BLAKE2s.

	
		PHP:
	
	
	
		
```
$data = "password";
$hash = hash("blake2s", $data);
$hashupper = strtoupper($hash)
```
