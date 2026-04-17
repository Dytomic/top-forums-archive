# 🪑Sit Button on the Fast Bar

**Category:** Source Development
**URL:** https://pkodev.com/threads/chairsit-button-on-the-fast-bar.148/
**Posts:** 1

---

## Original Post
**Author:** Grim4ik  
**Date:** 2026-03-06

Nowadays, many keyboards no longer include the **Insert** key. Because of this, you can conveniently add a **Sit** button directly to your fast action bar.

This guide explains how to implement it.

![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f4c2.png) Step 1 — Edit UIEquipForm.cpp

Open **UIEquipForm.cpp** and locate the following line:

	
		C++:
	
	
	
		
```
CForm* frmFast = _FindForm("frmFast");
```
