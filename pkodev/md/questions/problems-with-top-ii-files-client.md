# Problems with ToP II Files + Client

**URL:** https://pkodev.com/threads/problems-with-top-ii-files-client.123/
**Posts:** 5

---

## Original Post
**Author:** Alphavey  
**Date:** 2026-02-04

**Hello everyone,**

I have the **ToP2 server source files** and a **clean ToP2 client**. I’ve already set up the server, and all services appear to be running correctly. However, no matter how many times I try, the **client never connects to the server**.

I do have **working files for ToP1**, and everything works fine there, but when I try the same approach with **ToP2**, it doesn’t work at all.

I’m not sure if this issue is related to:

- the **IP changer**,

- hardcoded IPs inside the client, or

- differences in how ToP2 handles server connections compared to ToP1.

Does anyone here have **experience setting up a ToP2 private server** or know what differences I should look for compared to ToP1?

Any help or guidance would be greatly appreciated.

Thanks in advance!


---

### Reply #1
**Pixel** — 2026-02-04

Did u try compiling ServerSet.txt ?


---

### Reply #2
**Alphavey** — 2026-02-05

> 
	
		
			
				[Pixel said:](/goto/post?id=158)
			
		
	
	
		
		
		
			Did u try compiling ServerSet.txt ?
		
		
		Click to expand...


---

### Reply #3
**JustNobre** — 2026-02-08

likely client IP or some firewall in between


---

### Reply #4
**Mutator** — 2026-03-29

The gateway configuration file has an incorrect port in the client section. I can't connect either because I don't know the port number in the client.
