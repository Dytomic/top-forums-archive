# Tales of Pirate 2022 DX9

**Category:** Source
**URL:** https://pkodev.com/threads/tales-of-pirate-2022-dx9.126/
**Posts:** 89

---

## Original Post
**Author:** Mothanna  
**Date:** 2026-02-11

**About This Repository**​[](#-about-this-repository)**This repository contains the source code for *Tales of Pirate*, updated to DirectX 9. Over the past few years, we collaborated with several freelancers to modernize the engine from its original DX8 foundation.**​[](#-this-repository-contains-the-source-code-for-tales-of-pirate-updated-to-directx-9-over-the-past-few-years-we-collaborated-with-several-freelancers-to-modernize-the-engine-from-its-original-dx8-foundation)**In response to certain groups within the community profiting from leaked versions of this code, we have decided to make the source public for the benefit of all ****developers.**** Please note that we do not offer support for future bugs or technical issues.**

While the core DX9 upgrade is functional, it originated from a separate development branch; you may encounter minor inconsistencies. This remains an excellent starting point for new projects. Finally, we are not responsible for any legacy bugs or exploits present in the original code, as these were inherited from previous owners.​**Credits & Copyright**​[](#-credits-copyright)**Ownership & Contributions** All rights to the engine upgrades and source modifications belong to **[SatisfyTeam](https://satisfy.live/)**, **Mothannkh**, and the private benefactors who funded the project’s development but chose to remain anonymous.
**Terms of Use** This source is provided to the community for development purposes. While we encourage innovation, we ask that users respect the work put in by the team and the contributors who made this progress possible.​CURRENT SOURCE SPECIFICATIONS​[](#-current-source-specifications)**Core Engine & Networking**​
- Upgraded from DirectX 8 to DirectX 9​

- Client and Server built with VS 2022 (C++14)​

- TopNet source integration​

- RSA/AES connection encryption (Client/Server)​

- Encrypted .clu files​

- Core packets updated to use Smart Pointers​

- Anti-WPE and Anti-DDoS protection​

- Anti-Dupe system​

**Gameplay Systems**​
- Offline Stalls and Offline Mode​

- Full Mount System​

- Guild Bank with transaction logs​

- AuthorizedGM system​

- Reworked Jackpot system​

- In-game Shop remade (Classic style, 9 items per page)​

**User Interface & Features**​
- Multi-resolution support​

- 60 FPS toggle option​

- HP and SP bars displayable as values or percentages​

- World Map with Zoom In/Out​

- Drop Info with integrated Drop Filter​

- Right-click inventory menu options​

- Friend/Enemy combat modes​

- Visibility toggles for Effects, Apps, and Mounts​

**Scripting & Structure**​
- Restructured LUA folders for better organization​

- Balanced Vanilla LUA setup​

- Simplified file structure with intuitive variable and function names​

- Modular design for easy code migration (copy/paste friendly)

**Repository link **
**here**
**VS Config files**
**Here**​


---

### Reply #1
**k1d0123** — 2026-02-11

64 bytes ![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f440.png)


---

### Reply #2
**Pixel** — 2026-02-11

At last, these are now publicly available, a great starting point for beginners who want to learn. Please use these files and source responsibly, and avoid using them for selling, profit, or scams. For anyone utilizing these resources, remember to appreciate and respect the efforts of the developers who contributed to them. Let’s learn, create, and grow together responsibly! Good release mothanna you are the best ![:)](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f642.png)


---

### Reply #3
**iamkennd** — 2026-02-11

Amazing...


---

### Reply #4
**skulkills** — 2026-02-11

Excelente


---

### Reply #5
**iamkennd** — 2026-02-11

I got problem to build game sourcers :/

If anyone can help me, i'll be gratefully! Ty

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
			
		![1770842749921.webp](https://pkodev.com/attachments/1770842749921-webp.76/)
		![1770842776198.webp](https://pkodev.com/attachments/1770842776198-webp.77/)


---

### Reply #6
**Pixel** — 2026-02-11

> 
	
		
			
				[iamkennd said:](/goto/post?id=171)
			
		
	
	
		
		
		
			I got problem to build game sourcers :/

If anyone can help me, i'll be gratefully! Ty

[View attachment 76](https://pkodev.com/attachments/76/)[View attachment 77](https://pkodev.com/attachments/77/)
		
		
		Click to expand...


---

### Reply #7
**Pucca** — 2026-02-12

Has anyone been able to build it successfully?


---

### Reply #8
**Mothanna** — 2026-02-12

> 
	
		
			
				[iamkennd said:](/goto/post?id=171)
			
		
	
	
		
		
		
			I got problem to build game sourcers :/

If anyone can help me, i'll be gratefully! Ty

[View attachment 76](https://pkodev.com/attachments/76/)[View attachment 77](https://pkodev.com/attachments/77/)
		
		
		Click to expand...


---

### Reply #9
**Pucca** — 2026-02-12

Can build x64 too?


---

### Reply #10
**Mothanna** — 2026-02-12

> 
	
		
			
				[Pucca said:](/goto/post?id=175)
			
		
	
	
		
		
		
			Can build x64 too?
		
		
		Click to expand...


---

### Reply #11
**Pucca** — 2026-02-12

Thanks, i will try soon.


---

### Reply #12
**astrobomb** — 2026-02-12

64 bits Available soon xDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDD


---

### Reply #13
**iamkennd** — 2026-02-12

> 
	
		
			
				[Pixel said:](/goto/post?id=172)
			
		
	
	
		
		
		
			You need vs2022 and this config to build. [https://drive.google.com/file/d/1H3X4FlIzeSGpNQKUh-ph0WZQ7Api8LNa/](https://drive.google.com/file/d/1H3X4FlIzeSGpNQKUh-ph0WZQ7Api8LNa/)
		
		
		Click to expand...


---

### Reply #14
**estrangulador** — 2026-02-12

vsual 2026 vai abrir o projeto ?


---

### Reply #15
**zLuke** — 2026-02-12

Thanks, **Mothannkh.

		![2026-02-12_02-55-06.webp](https://pkodev.com/attachments/2026-02-12_02-55-06-webp.83/)**


---

### Reply #16
**iamkennd** — 2026-02-12

1st Step i did: Build layer > Configuration manager and set to x86 (32bits)

		![1770854425612.webp](https://pkodev.com/attachments/1770854425612-webp.85/)

2nd step i did: Close conf manager layer and built solution

		![1770854523834.webp](https://pkodev.com/attachments/1770854523834-webp.86/)

**So i got this error: **​[](#-so-i-got-this-error)

		![1770854569257.webp](https://pkodev.com/attachments/1770854569257-webp.87/)

**I was using version 2013 but i already installed MFC and Built tools already installed.**

		![1770854635911.webp](https://pkodev.com/attachments/1770854635911-webp.88/)

Maybe i need to install those MSVC v140-142 right?


---

### Reply #17
**estrangulador** — 2026-02-12

Can you provide a solution for this?

		![1770860927367.webp](https://pkodev.com/attachments/1770860927367-webp.93/)


---

### Reply #18
**Mothanna** — 2026-02-12

> 
	
		
			
				[estrangulador said:](/goto/post?id=184)
			
		
	
	
		
		
		
			Can you provide a solution for this?
[View attachment 93](https://pkodev.com/attachments/93/)
		
		
		Click to expand...


---

### Reply #19
**Mothanna** — 2026-02-12

> 
	
		
			
				[iamkennd said:](/goto/post?id=183)
			
		
	
	
		
		
		
			1st Step i did: Build layer > Configuration manager and set to x86 (32bits)

[View attachment 85](https://pkodev.com/attachments/85/)

2nd step i did: Close conf manager layer and built solution

[View attachment 86](https://pkodev.com/attachments/86/)

**So i got this error: **​
[View attachment 87](https://pkodev.com/attachments/87/)

**I was using version 2013 but i already installed MFC and Built tools already installed.**

[View attachment 88](https://pkodev.com/attachments/88/)

Maybe i need to install those MSVC v140-142 right?
		
		
		Click to expand...


---

### Reply #20
**Pucca** — 2026-02-12

> 
	
		
			
				[estrangulador said:](/goto/post?id=184)
			
		
	
	
		
		
		
			Can you provide a solution for this?
[View attachment 93](https://pkodev.com/attachments/93/)
		
		
		Click to expand...


---

### Reply #21
**Pixel** — 2026-02-12

> 
	
		
			
				[iamkennd said:](/goto/post?id=180)
			
		
	
	
		
		
		
			Sup brother, hope everything ok!

Bro, the link you sent hasnt any file, could you send me right link or fix link?

Thats what happening:
[View attachment 80](https://pkodev.com/attachments/80/)

Grateful.
		
		
		Click to expand...


---

### Reply #22
**washimingo** — 2026-02-12

awesome work, thank!!!


---

### Reply #23
**iamkennd** — 2026-02-13

> 
	
		
			
				[Pixel said:](/goto/post?id=188)
			
		
	
	
		
		
		
			Try this out now [https://drive.google.com/file/d/1GR8GdSNe-UocUNpkvChoHBaqZJaTcuuS/view?usp=sharing](https://drive.google.com/file/d/1GR8GdSNe-UocUNpkvChoHBaqZJaTcuuS/view?usp=sharing)
		
		
		Click to expand...


---

### Reply #24
**zLuke** — 2026-02-13

Use the Release configuration, as the Debug configuration does not include the USE_DX_VERSION;LW_USE_DX9;DIRECT3D_VERSION=0x0900 compilation directives, and the build is performed using DirectX8


---

### Reply #25
**iamkennd** — 2026-02-13

> 
	
		
			
				[zLuke said:](/goto/post?id=192)
			
		
	
	
		
		
		
			Use the Release configuration, as the Debug configuration does not include the USE_DX_VERSION;LW_USE_DX9;DIRECT3D_VERSION=0x0900 compilation directives, and the build is performed using DirectX8
		
		
		Click to expand...


---

### Reply #26
**skulkills** — 2026-02-13

> 
	
		
			
				[iamkennd said:](/goto/post?id=193)
			
		
	
	
		
		
		
			**tried but got this, can u help me?**

[View attachment 97](https://pkodev.com/attachments/97/)
		
		
		Click to expand...


---

### Reply #27
**iamkennd** — 2026-02-13

> 
	
		
			
				[skulkills said:](/goto/post?id=195)
			
		
	
	
		
		
		
			Mostra como está ai a versão do MFC? lá em componentes individuais
		
		
		Click to expand...


---

### Reply #28
**Zakernado** — 2026-02-13

A very good release!

Thank you for your contribution to the community!


---

### Reply #29
**skulkills** — 2026-02-14

> 
	
		
			
				[iamkennd said:](/goto/post?id=196)
			
		
	
	
		
		
		
			Agora, meu patrão!

[View attachment 101](https://pkodev.com/attachments/101/)[View attachment 102](https://pkodev.com/attachments/102/)

Você poderia me chamar no discord? Estou querendo mt ligar esse servidor e tentar desenvolver uma file.

Caso sim, meu discord é: iamkennd
		
		
		Click to expand...


---

### Reply #30
**Senzuki** — 2026-02-14

How can i fix it? 
		![1771082684521.webp](https://pkodev.com/attachments/1771082684521-webp.105/)


---

### Reply #31
**estrangulador** — 2026-02-14

Is it possible to upload the discord-rpc.lib files?

-------------

13>LINK: fatal error LNK1181: could not open input file 'discord-rpc.lib'

13>Project build ready "kop.vcxproj" -- FAILED.

========== Recompile All: 12 successful, 1 failed, 0 skipped ==========


---

### Reply #32
**zLuke** — 2026-02-14

> 
	
		
			
				[estrangulador said:](/goto/post?id=200)
			
		
	
	
		
		
		
			Is it possible to upload the discord-rpc.lib files?

-------------

13>LINK: fatal error LNK1181: could not open input file 'discord-rpc.lib'

13>Project build ready "kop.vcxproj" -- FAILED.

========== Recompile All: 12 successful, 1 failed, 0 skipped ==========
		
		
		Click to expand...


---

### Reply #33
**mudoek** — 2026-02-14

how to create account by website ? md5 doesnt work .


---

### Reply #34
**Mothanna** — 2026-02-14

> 
	
		
			
				[mudoek said:](/goto/post?id=202)
			
		
	
	
		
		
		
			how to create account by website ? md5 doesnt work .
		
		
		Click to expand...


---

### Reply #35
**Mothanna** — 2026-02-14

> 
	
		
			
				[estrangulador said:](/goto/post?id=200)
			
		
	
	
		
		
		
			Is it possible to upload the discord-rpc.lib files?

-------------

13>LINK: fatal error LNK1181: could not open input file 'discord-rpc.lib'

13>Project build ready "kop.vcxproj" -- FAILED.

========== Recompile All: 12 successful, 1 failed, 0 skipped ==========
		
		
		Click to expand...


---

### Reply #36
**Senzuki** — 2026-02-15

> 
	
		
			
				[Senzuki said:](/goto/post?id=199)
			
		
	
	
		
		
		
			How can i fix it? [View attachment 105](https://pkodev.com/attachments/105/)
		
		
		Click to expand...


---

### Reply #37
**Mothanna** — 2026-02-15

> 
	
		
			
				[Senzuki said:](/goto/post?id=206)
			
		
	
	
		
		
		
			any tips?
		
		
		Click to expand...


---

### Reply #38
**Senzuki** — 2026-02-15

Still something missing.
		![1771118970389.webp](https://pkodev.com/attachments/1771118970389-webp.111/)


---

### Reply #39
**Mothanna** — 2026-02-15

> 
	
		
			
				[Senzuki said:](/goto/post?id=208)
			
		
	
	
		
		
		
			Still something missing.[View attachment 111](https://pkodev.com/attachments/111/)
		
		
		Click to expand...


---

### Reply #40
**Senzuki** — 2026-02-15

Still cant build successfully. icudt.lib, icuucd.lib is missing or cant open.(for debug x86)

for release x86:
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
			
		![1771166908098.webp](https://pkodev.com/attachments/1771166908098-webp.113/)


---

### Reply #41
**zLuke** — 2026-02-15

[
						icu.zip
					]()
				

				

				
					
						
							![drive.google.com](https://ssl.gstatic.com/images/branding/product/1x/drive_2020q4_32dp.png)
					drive.google.com


---

### Reply #42
**Pucca** — 2026-02-15

> 
	
		
			
				[zLuke said:](/goto/post?id=211)
			
		
	
	
		
		
		
			
	

	
		
			
			
				
					[
						icu.zip
					]()
				

				

				
					
						
							![drive.google.com](https://ssl.gstatic.com/images/branding/product/1x/drive_2020q4_32dp.png)
					drive.google.com


---

### Reply #43
**zLuke** — 2026-02-15

> 
	
		
			
				[Pucca said:](/goto/post?id=212)
			
		
	
	
		
		
		
			Need access to download
		
		
		Click to expand...


---

### Reply #44
**Pucca** — 2026-02-15

Thanks, i will try soon [@Senzuki](https://pkodev.com/members/136/)


---

### Reply #45
**iamkennd** — 2026-02-15

> 
	
		
			
				[skulkills said:](/goto/post?id=198)
			
		
	
	
		
		
		
			Olha eu não uso discord mais vou fazer vídeos em um canal do youtube vou postar depois aqui no fórum também, mais no caso seu caso pelo print que você tirou da para ver claramente que suas ferramentas de compilação esta como v143 quando precisa da v142
		
		
		Click to expand...


---

### Reply #46
**lexbergeron** — 2026-02-16

Thank you so much ! you are very awsome !


---

### Reply #47
**JustNobre** — 2026-02-16

how do I modify the IP of the client?

IP changer isn't working and I forgot the file location


---

### Reply #48
**Grim4ik** — 2026-02-16

> 
	
		
			
				[JustNobre said:](/goto/post?id=217)
			
		
	
	
		
		
		
			how do I modify the IP of the client?

IP changer isn't working and I forgot the file location
		
		
		Click to expand...


---

### Reply #49
**JustNobre** — 2026-02-16

> 
	
		
			
				[Grim4ik said:](/goto/post?id=218)
			
		
	
	
		
		
		
			scripts/table/serverset
		
		
		Click to expand...


---

### Reply #50
**JustNobre** — 2026-02-19

how do I fix time zone? clock is correct but not for my time zone

do we have the jackpot NPC already on the map?


---

### Reply #51
**ihaspiez** — 2026-02-19

I hate to be a noob but, I'm stuck at getting the client connecting with the server ![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f605.png) IP Changer wasn't doing anything ( actually think that ip changer breaks the client ) changed the serverset.txt in the table folder and compiled it (deleted serverset.bin) but this still is trying to reach another server that is nowhere to be seen that I could find on the client anyone have idea on this?


---

### Reply #52
**Mothanna** — 2026-02-19

> 
	
		
			
				[ihaspiez said:](/goto/post?id=232)
			
		
	
	
		
		
		
			I hate to be a noob but, I'm stuck at getting the client connecting with the server ![image](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f605.png) IP Changer wasn't doing anything ( actually think that ip changer breaks the client ) changed the serverset.txt in the table folder and compiled it (deleted serverset.bin) but this still is trying to reach another server that is nowhere to be seen that I could find on the client anyone have idea on this?
		
		
		Click to expand...


---

### Reply #53
**iamkennd** — 2026-02-19

> 
	
		
			
				[Mothanna said:](/goto/post?id=235)
			
		
	
	
		
		
		
			serverset nothing else
		
		
		Click to expand...


---

### Reply #54
**ihaspiez** — 2026-02-19

> 
	
		
			
				[Mothanna said:](/goto/post?id=235)
			
		
	
	
		
		
		
			serverset nothing else
		
		
		Click to expand...


---

### Reply #55
**zLuke** — 2026-02-20

![Poezies](/data/avatars/s/0/17.jpg?1769285845)
	
	
		
			
				Setup Guide
			
			[Thread 'Tales of Pirates Server Setup Guide 2026'](/threads/tales-of-pirates-server-setup-guide-2026.13/)
		

		
			Jan 24, 2026


---

### Reply #56
**jetville08** — 2026-02-20

What Version of MSSQL is used in this Source?


---

### Reply #57
**Mdr** — 2026-02-20

[@Mothanna](https://pkodev.com/members/20/) I urge you to change this to an MIT License. There are several contributions here made by me and Snre3n, and I was not contacted at all for this release. In fact, I am pretty sure this version of CO (2021) was actually leaked/sold within our team at the time. I respect the other contributors but didn't want this laying around for several reasons (which is why me and Snre3n/Ogge released YATOPS).

	
		C++:
	
	
	
		
```
if (g_rsaaes) // RSA-AES Network Encryption by Mdr - CO 2021
```


---

### Reply #58
**Mothanna** — 2026-02-20

> 
	
		
			
				[Mdr said:](/goto/post?id=261)
			
		
	
	
		
		
		
			[@Mothanna](https://pkodev.com/members/20/) I urge you to change this to an MIT License. There are several contributions here made by me and Snre3n, and I was not contacted at all for this release. In fact, I am pretty sure this version of CO (2021) was actually leaked/sold within our team at the time. I respect the other contributors but didn't want this laying around for several reasons (which is why me and Snre3n/Ogge released YATOPS).

	
		C++:
	
	
	
		
```
if (g_rsaaes) // RSA-AES Network Encryption by Mdr - CO 2021
```


---

### Reply #59
**Mothanna** — 2026-02-20

> 
	
		
			
				[jetville08 said:](/goto/post?id=244)
			
		
	
	
		
		
		
			What Version of MSSQL is used in this Source?
		
		
		Click to expand...


---

### Reply #60
**Mdr** — 2026-02-21

> 
	
		
			
				[Mothanna said:](/goto/post?id=263)
			
		
	
	
		
		
		
			we are not using this at our end tbh main reason this been release that dx9 we sold to someone was installed to this source, and been leaked with source full package selling for 200$ and the same dumb who selling it shared this back to me , so better be free for development than abused selling to others

and i mentioned in first post , we won't support any bug /leak just take what u want , leave what u don't neeed, even it have some bugs can be fixed with ai nowadays tbh
		
		
		Click to expand...


---

### Reply #61
**jetville08** — 2026-02-21

> 
	
		
			
				[Mothanna said:](/goto/post?id=264)
			
		
	
	
		
		
		
			2019, u could try 2020 but query i bet too old for this u may check toprecode for 2020 refactor
		
		
		Click to expand...


---

### Reply #62
**Mothanna** — 2026-02-21

> 
	
		
			
				[Mdr said:](/goto/post?id=286)
			
		
	
	
		
		
		
			I see. But still, please add our names to the list of contributors. I was simply pinpoiting the exact issues with this source in case someone wants to take a stab at it. Namely, memory leaks in LIBDBC/GateServer and crashes due to memory fragmentation (can't recall if we ported this version to x64).
		
		
		Click to expand...


---

### Reply #63
**iamkennd** — 2026-02-22

> 
	
		
			
				[Mothanna said:](/goto/post?id=166)
			
		
	
	
		
		
		
			**About This Repository**​**This repository contains the source code for *Tales of Pirate*, updated to DirectX 9. Over the past few years, we collaborated with several freelancers to modernize the engine from its original DX8 foundation.**​**In response to certain groups within the community profiting from leaked versions of this code, we have decided to make the source public for the benefit of all ****developers.**** Please note that we do not offer support for future bugs or technical issues.**

While the core DX9 upgrade is functional, it originated from a separate development branch; you may encounter minor inconsistencies. This remains an excellent starting point for new projects. Finally, we are not responsible for any legacy bugs or exploits present in the original code, as these were inherited from previous owners.​**Credits & Copyright**​**Ownership & Contributions** All rights to the engine upgrades and source modifications belong to **[SatisfyTeam](https://satisfy.live/)**, **Mothannkh**, and the private benefactors who funded the project’s development but chose to remain anonymous.
**Terms of Use** This source is provided to the community for development purposes. While we encourage innovation, we ask that users respect the work put in by the team and the contributors who made this progress possible.​CURRENT SOURCE SPECIFICATIONS​**Core Engine & Networking**​
- Upgraded from DirectX 8 to DirectX 9​

- Client and Server built with VS 2022 (C++14)​

- TopNet source integration​

- RSA/AES connection encryption (Client/Server)​

- Encrypted .clu files​

- Core packets updated to use Smart Pointers​

- Anti-WPE and Anti-DDoS protection​

- Anti-Dupe system​

**Gameplay Systems**​
- Offline Stalls and Offline Mode​

- Full Mount System​

- Guild Bank with transaction logs​

- AuthorizedGM system​

- Reworked Jackpot system​

- In-game Shop remade (Classic style, 9 items per page)​

**User Interface & Features**​
- Multi-resolution support​

- 60 FPS toggle option​

- HP and SP bars displayable as values or percentages​

- World Map with Zoom In/Out​

- Drop Info with integrated Drop Filter​

- Right-click inventory menu options​

- Friend/Enemy combat modes​

- Visibility toggles for Effects, Apps, and Mounts​

**Scripting & Structure**​
- Restructured LUA folders for better organization​

- Balanced Vanilla LUA setup​

- Simplified file structure with intuitive variable and function names​

- Modular design for easy code migration (copy/paste friendly)

**Repository link **
**here**
**VS Config files**
**Here**​

		Click to expand...


---

### Reply #64
**Mothanna** — 2026-02-24

> 
	
		
			
				[iamkennd said:](/goto/post?id=320)
			
		
	
	
		
		
		
			Hello.

I saw is missing for LUA files, can u upload it please?
		
		
		Click to expand...


---

### Reply #65
**iamkennd** — 2026-02-24

> 
	
		
			
				[Mothanna said:](/goto/post?id=322)
			
		
	
	
		
		
		
			which lua files?
		
		
		Click to expand...


---

### Reply #66
**Mothanna** — 2026-02-24

> 
	
		
			
				[iamkennd said:](/goto/post?id=323)
			
		
	
	
		
		
		
			theres no LUA folder, just addons
		
		
		Click to expand...


---

### Reply #67
**hpgutopiamagician** — 2026-03-03

Hello! not sure if this is the right place but it relates to these server files..

any one experience glows not fulling working, or partially rendering? usually have to teleport / unequip, re-equip ring/cloak for glows to work. on the left you can see the cloak glow not fully rendering compared to the right. 

any help would be appreciated! thanks^^

		![1772547106434.webp](https://pkodev.com/attachments/1772547106434-webp.274/)


---

### Reply #68
**JustNobre** — 2026-03-04

> 
	
		
			
				[hpgutopiamagician said:](/goto/post?id=337)
			
		
	
	
		
		
		
			Hello! not sure if this is the right place but it relates to these server files..

any one experience glows not fulling working, or partially rendering? usually have to teleport / unequip, re-equip ring/cloak for glows to work. on the left you can see the cloak glow not fully rendering compared to the right.

any help would be appreciated! thanks^^
		
		
		Click to expand...


---

### Reply #69
**hpgutopiamagician** — 2026-03-04

> 
	
		
			
				[JustNobre said:](/goto/post?id=341)
			
		
	
	
		
		
		
			My admiral clock not on the right spot and doesnt have glow
[View attachment 278](https://pkodev.com/attachments/278/)
		
		
		Click to expand...


---

### Reply #70
**alexxst** — 2026-03-12

![1773266925858.webp](https://pkodev.com/attachments/1773266925858-webp.306/)

Who can tell me why this happened in this client?


---

### Reply #71
**Poezies** — 2026-03-12

Solid release!


---

### Reply #72
**zLuke** — 2026-03-12

> 
	
		
			
				[alexxst said:](/goto/post?id=368)
			
		
	
	
		
		
		
			Who can tell me why this happened in this client?
		
		
		Click to expand...


---

### Reply #73
**[TwT]~Darkness** — 2026-03-12

So, guys. I've been looking around... Please tell me, will there be any problems if I use the old version of SQLR2 2008? Or should I use something newer? I once had problems finding and installing it for various unknown reasons.


---

### Reply #74
**JustNobre** — 2026-03-12

> 
	
		
			
				[[TwT]~Darkness said:](/goto/post?id=389)
			
		
	
	
		
		
		
			So, guys. I've been looking around... Please tell me, will there be any problems if I use the old version of SQLR2 2008? Or should I use something newer? I once had problems finding and installing it for various unknown reasons.
		
		
		Click to expand...


---

### Reply #75
**saa0d** — 2026-03-19

> 
	
		
			
				[Mothanna said:](/goto/post?id=166)
			
		
	
	
		
		
		
			**About This Repository**​**This repository contains the source code for *Tales of Pirate*, updated to DirectX 9. Over the past few years, we collaborated with several freelancers to modernize the engine from its original DX8 foundation.**​**In response to certain groups within the community profiting from leaked versions of this code, we have decided to make the source public for the benefit of all ****developers.**** Please note that we do not offer support for future bugs or technical issues.**

While the core DX9 upgrade is functional, it originated from a separate development branch; you may encounter minor inconsistencies. This remains an excellent starting point for new projects. Finally, we are not responsible for any legacy bugs or exploits present in the original code, as these were inherited from previous owners.​**Credits & Copyright**​**Ownership & Contributions** All rights to the engine upgrades and source modifications belong to **[SatisfyTeam](https://satisfy.live/)**, **Mothannkh**, and the private benefactors who funded the project’s development but chose to remain anonymous.
**Terms of Use** This source is provided to the community for development purposes. While we encourage innovation, we ask that users respect the work put in by the team and the contributors who made this progress possible.​CURRENT SOURCE SPECIFICATIONS​**Core Engine & Networking**​
- Upgraded from DirectX 8 to DirectX 9​

- Client and Server built with VS 2022 (C++14)​

- TopNet source integration​

- RSA/AES connection encryption (Client/Server)​

- Encrypted .clu files​

- Core packets updated to use Smart Pointers​

- Anti-WPE and Anti-DDoS protection​

- Anti-Dupe system​

**Gameplay Systems**​
- Offline Stalls and Offline Mode​

- Full Mount System​

- Guild Bank with transaction logs​

- AuthorizedGM system​

- Reworked Jackpot system​

- In-game Shop remade (Classic style, 9 items per page)​

**User Interface & Features**​
- Multi-resolution support​

- 60 FPS toggle option​

- HP and SP bars displayable as values or percentages​

- World Map with Zoom In/Out​

- Drop Info with integrated Drop Filter​

- Right-click inventory menu options​

- Friend/Enemy combat modes​

- Visibility toggles for Effects, Apps, and Mounts​

**Scripting & Structure**​
- Restructured LUA folders for better organization​

- Balanced Vanilla LUA setup​

- Simplified file structure with intuitive variable and function names​

- Modular design for easy code migration (copy/paste friendly)

**Repository link **
**here**
**VS Config files**
**Here**​

		Click to expand...


---

### Reply #76
**saa0d** — 2026-03-20

> 
	
		
			
				[saa0d said:](/goto/post?id=396)
			
		
	
	
		
		
		
			Hi, thank you for a great release. I was trying to do this myself late last year but failed miserably with AI lol. I opened the client sln file and saw that it had many missing files due to broken paths. I renamed Libraries folder to CommonLib (coz thats where the solution files were trying to access and majority of them got fixed). when i was trying to rebuild the game project (from the kop solution) it was giving me a file not found error, which was util.h. i realized later that it's not properly accessing the folder that has the include files. So when I went to that folder, I saw that util.sln is still based on the legacy Visual studio (2003); is this intentional, or was there no need for it to be upgraded to VS2022? There are some other sln files too still based on the old VS like the mindpower sln file.

Edit: As my experience with TOP server dev is so rusty (pre 2016), I think I understood something about the structure of the KOP solution. It seems to me that the solution was migrated to 2022, and the KOP sln file serves as a central solution to edit/build all other dependecies such as the mindpower engine, client, cryptlib, etc.. is that right?
		
		
		Click to expand...


---

### Reply #77
**Mothanna** — 2026-03-20

you just have to open talesofpirates.sln and build nothing else


---

### Reply #78
**mudoek** — 2026-03-23

anyone know how to fix this ? the character model dont load. on this section of the client

		![Screenshot_10.webp](https://pkodev.com/attachments/screenshot_10-webp.334/)


---

### Reply #79
**zLuke** — 2026-03-23

After rendering a 3D scene, values remain in the depth buffer, and the character preview in the UI is rendered with a regular Z-test and fog. In DX9, this causes the model to be clipped by depth (or "sunk" in the fog) and visually disappear.

In RenderCha, before rendering the model to the UI, we forcefully configure the pipeline: we disable fog (FOGENABLE), make the depth test always pass (ZFUNC = ALWAYS), and disable writing to the Z-buffer (ZWRITEENABLE = FALSE), and we reset the blending/alpha test, color vertices, culling, and texture stages to a predictable state. After rendering, all these states are restored.

In file CreateChaScene.cpp replace the entire CCreateChaScene::RenderCha function with this code:

	
		C++:
	
	
	
		
```
void CCreateChaScene::RenderCha(int x,int y)
{
 if (m_nSelChaIndex < 0 || m_nSelChaIndex > 3)
 return;
 if( !m_pChaForUI[m_nSelChaIndex] )
 return;

 DWORD oldZEnable = 0;
 DWORD oldZWriteEnable = 0;
 DWORD oldZFunc = 0;
 DWORD oldFogEnable = 0;
 DWORD oldAlphaBlendEnable = 0;
 DWORD oldSrcBlend = 0;
 DWORD oldDestBlend = 0;
 DWORD oldAlphaTestEnable = 0;
 DWORD oldColorVertex = 0;
 DWORD oldCullMode = 0;

 g_Render.GetRenderState(D3DRS_ZENABLE, &oldZEnable);
 g_Render.GetRenderState(D3DRS_ZWRITEENABLE, &oldZWriteEnable);
 g_Render.GetRenderState(D3DRS_ZFUNC, &oldZFunc);
 g_Render.GetRenderState(D3DRS_FOGENABLE, &oldFogEnable);
 g_Render.GetRenderState(D3DRS_ALPHABLENDENABLE, &oldAlphaBlendEnable);
 g_Render.GetRenderState(D3DRS_SRCBLEND, &oldSrcBlend);
 g_Render.GetRenderState(D3DRS_DESTBLEND, &oldDestBlend);
 g_Render.GetRenderState(D3DRS_ALPHATESTENABLE, &oldAlphaTestEnable);
 g_Render.GetRenderState(D3DRS_COLORVERTEX, &oldColorVertex);
 g_Render.GetRenderState(D3DRS_CULLMODE, &oldCullMode);

 g_Render.SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
 g_Render.SetRenderState(D3DRS_ZWRITEENABLE, FALSE);
 g_Render.SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);
 g_Render.SetRenderState(D3DRS_FOGENABLE, FALSE);
 g_Render.SetRenderState(D3DRS_ALPHABLENDENABLE, FALSE);
 g_Render.SetRenderState(D3DRS_SRCBLEND, D3DBLEND_ONE);
 g_Render.SetRenderState(D3DRS_DESTBLEND, D3DBLEND_ZERO);
 g_Render.SetRenderState(D3DRS_ALPHATESTENABLE, FALSE);
 g_Render.SetRenderState(D3DRS_COLORVERTEX, FALSE);
 g_Render.SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
 g_Render.SetRenderState(D3DRS_TEXTUREFACTOR, 0xffffffff);

 // Reset stage 0 to a deterministic pipeline for DX9 UI 3D draw.
 g_Render.SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);
 g_Render.SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
 g_Render.SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE);
 g_Render.SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE);
 g_Render.SetTextureStageState(0, D3DTSS_ALPHAARG2, D3DTA_DIFFUSE);
 g_Render.SetTextureStageState(0, D3DTSS_ALPHAOP, D3DTOP_MODULATE);
 g_Render.SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_DISABLE);
 g_Render.SetTextureStageState(1, D3DTSS_ALPHAOP, D3DTOP_DISABLE);

 g_Render.LookAt( D3DXVECTOR3( 11.0f, 36.0f, 10.0f ), D3DXVECTOR3( 8.70f, 12.0f, 8.0f ), MPRender::VIEW_3DUI );
 y +=100;

 MPMatrix44 old_mat = *m_pChaForUI[m_nSelChaIndex]->GetMatrix();
 m_pChaForUI[m_nSelChaIndex]->SetUIYaw(180 + m_nChaRotate);
 m_pChaForUI[m_nSelChaIndex]->SetUIScaleDis(9.0f * g_Render.GetScrWidth()/TINY_RES_X );
 m_pChaForUI[m_nSelChaIndex]->RenderForUI(x, y);
 m_pChaForUI[m_nSelChaIndex]->SetMatrix(&old_mat);

 g_Render.SetTransformView(&g_Render.GetWorldViewMatrix());

 g_Render.SetRenderState(D3DRS_ZENABLE, oldZEnable);
 g_Render.SetRenderState(D3DRS_ZWRITEENABLE, oldZWriteEnable);
 g_Render.SetRenderState(D3DRS_ZFUNC, oldZFunc);
 g_Render.SetRenderState(D3DRS_FOGENABLE, oldFogEnable);
 g_Render.SetRenderState(D3DRS_ALPHABLENDENABLE, oldAlphaBlendEnable);
 g_Render.SetRenderState(D3DRS_SRCBLEND, oldSrcBlend);
 g_Render.SetRenderState(D3DRS_DESTBLEND, oldDestBlend);
 g_Render.SetRenderState(D3DRS_ALPHATESTENABLE, oldAlphaTestEnable);
 g_Render.SetRenderState(D3DRS_COLORVERTEX, oldColorVertex);
 g_Render.SetRenderState(D3DRS_CULLMODE, oldCullMode);

}
```


---

### Reply #80
**[TwT]~Darkness** — 2026-03-24

> 
	
		
			
				[estrangulador said:](/goto/post?id=184)
			
		
	
	
		
		
		
			Can you provide a solution for this?
[View attachment 93](https://pkodev.com/attachments/93/)
		
		
		Click to expand...


---

### Reply #81
**habs8024** — 2026-03-29

> 
	
		
			
				[mudoek said:](/goto/post?id=202)
			
		
	
	
		
		
		
			how to create account by website ? md5 doesnt work .
		
		
		Click to expand...


---

### Reply #82
**alexxst** — 2026-03-29

who will use the server, remove the CMD_CM_KITBAGTEMPlocks command, which is a backdoor for executing any lua code without verification.


---

### Reply #83
**habs8024** — 2026-04-02

> 
	
		
			
				[zLuke said:](/goto/post?id=413)
			
		
	
	
		
		
		
			After rendering a 3D scene, values remain in the depth buffer, and the character preview in the UI is rendered with a regular Z-test and fog. In DX9, this causes the model to be clipped by depth (or "sunk" in the fog) and visually disappear.

In RenderCha, before rendering the model to the UI, we forcefully configure the pipeline: we disable fog (FOGENABLE), make the depth test always pass (ZFUNC = ALWAYS), and disable writing to the Z-buffer (ZWRITEENABLE = FALSE), and we reset the blending/alpha test, color vertices, culling, and texture stages to a predictable state. After rendering, all these states are restored.

In file CreateChaScene.cpp replace the entire CCreateChaScene::RenderCha function with this code:

	
		C++:
	
	
	
		
```
void CCreateChaScene::RenderCha(int x,int y)
{
 if (m_nSelChaIndex < 0 || m_nSelChaIndex > 3)
 return;
 if( !m_pChaForUI[m_nSelChaIndex] )
 return;

 DWORD oldZEnable = 0;
 DWORD oldZWriteEnable = 0;
 DWORD oldZFunc = 0;
 DWORD oldFogEnable = 0;
 DWORD oldAlphaBlendEnable = 0;
 DWORD oldSrcBlend = 0;
 DWORD oldDestBlend = 0;
 DWORD oldAlphaTestEnable = 0;
 DWORD oldColorVertex = 0;
 DWORD oldCullMode = 0;

 g_Render.GetRenderState(D3DRS_ZENABLE, &oldZEnable);
 g_Render.GetRenderState(D3DRS_ZWRITEENABLE, &oldZWriteEnable);
 g_Render.GetRenderState(D3DRS_ZFUNC, &oldZFunc);
 g_Render.GetRenderState(D3DRS_FOGENABLE, &oldFogEnable);
 g_Render.GetRenderState(D3DRS_ALPHABLENDENABLE, &oldAlphaBlendEnable);
 g_Render.GetRenderState(D3DRS_SRCBLEND, &oldSrcBlend);
 g_Render.GetRenderState(D3DRS_DESTBLEND, &oldDestBlend);
 g_Render.GetRenderState(D3DRS_ALPHATESTENABLE, &oldAlphaTestEnable);
 g_Render.GetRenderState(D3DRS_COLORVERTEX, &oldColorVertex);
 g_Render.GetRenderState(D3DRS_CULLMODE, &oldCullMode);

 g_Render.SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
 g_Render.SetRenderState(D3DRS_ZWRITEENABLE, FALSE);
 g_Render.SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);
 g_Render.SetRenderState(D3DRS_FOGENABLE, FALSE);
 g_Render.SetRenderState(D3DRS_ALPHABLENDENABLE, FALSE);
 g_Render.SetRenderState(D3DRS_SRCBLEND, D3DBLEND_ONE);
 g_Render.SetRenderState(D3DRS_DESTBLEND, D3DBLEND_ZERO);
 g_Render.SetRenderState(D3DRS_ALPHATESTENABLE, FALSE);
 g_Render.SetRenderState(D3DRS_COLORVERTEX, FALSE);
 g_Render.SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
 g_Render.SetRenderState(D3DRS_TEXTUREFACTOR, 0xffffffff);

 // Reset stage 0 to a deterministic pipeline for DX9 UI 3D draw.
 g_Render.SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);
 g_Render.SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
 g_Render.SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE);
 g_Render.SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE);
 g_Render.SetTextureStageState(0, D3DTSS_ALPHAARG2, D3DTA_DIFFUSE);
 g_Render.SetTextureStageState(0, D3DTSS_ALPHAOP, D3DTOP_MODULATE);
 g_Render.SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_DISABLE);
 g_Render.SetTextureStageState(1, D3DTSS_ALPHAOP, D3DTOP_DISABLE);

 g_Render.LookAt( D3DXVECTOR3( 11.0f, 36.0f, 10.0f ), D3DXVECTOR3( 8.70f, 12.0f, 8.0f ), MPRender::VIEW_3DUI );
 y +=100;

 MPMatrix44 old_mat = *m_pChaForUI[m_nSelChaIndex]->GetMatrix();
 m_pChaForUI[m_nSelChaIndex]->SetUIYaw(180 + m_nChaRotate);
 m_pChaForUI[m_nSelChaIndex]->SetUIScaleDis(9.0f * g_Render.GetScrWidth()/TINY_RES_X );
 m_pChaForUI[m_nSelChaIndex]->RenderForUI(x, y);
 m_pChaForUI[m_nSelChaIndex]->SetMatrix(&old_mat);

 g_Render.SetTransformView(&g_Render.GetWorldViewMatrix());

 g_Render.SetRenderState(D3DRS_ZENABLE, oldZEnable);
 g_Render.SetRenderState(D3DRS_ZWRITEENABLE, oldZWriteEnable);
 g_Render.SetRenderState(D3DRS_ZFUNC, oldZFunc);
 g_Render.SetRenderState(D3DRS_FOGENABLE, oldFogEnable);
 g_Render.SetRenderState(D3DRS_ALPHABLENDENABLE, oldAlphaBlendEnable);
 g_Render.SetRenderState(D3DRS_SRCBLEND, oldSrcBlend);
 g_Render.SetRenderState(D3DRS_DESTBLEND, oldDestBlend);
 g_Render.SetRenderState(D3DRS_ALPHATESTENABLE, oldAlphaTestEnable);
 g_Render.SetRenderState(D3DRS_COLORVERTEX, oldColorVertex);
 g_Render.SetRenderState(D3DRS_CULLMODE, oldCullMode);

}
```


---

### Reply #84
**2730278QQ** — 2026-04-09

Can you help me translate it into Chinese? I am a Chinese player. Thank you very much for sharing the source code. Thank you


---

### Reply #85
**DiosL** — 2026-04-13

Source x64 avaible for the community ?


---

### Reply #86
**a112311** — 2026-04-15

Bro, regarding the MSVC settings you mentioned — using v142 and C++14 for compilation, but I keep getting errors when selecting these two options. I noticed that in the Client code, the kop.vcxproj file specifies <PlatformToolset>v143</PlatformToolset> and <LanguageStandard>stdcpplatest</LanguageStandard>. Does this mean I need to select MSVC v143 and C++ stdcpplatest? Now I’m a bit confused about how to choose these settings.


---

### Reply #87
**alexxst** — 2026-04-15

Install the latest C++ and enjoy the build. Everything goes smoothly.


---

### Reply #88
**a112311** — 2026-04-16

Bro, thank you very much for your help. I'll try again.
