# Resurrection at the place of death

**Category:** Source Development
**URL:** https://pkodev.com/threads/resurrection-at-the-place-of-death.156/
**Posts:** 10

---

## Original Post
**Author:** zLuke  
**Date:** 2026-03-22

Resurrection at the place of death​[](#-resurrection-at-the-place-of-death)


---

### Reply #1
**zLuke** — 2026-03-22

Disable on-site resurrection if the character is on a ship, as it doesn't work anyway.
Replace in the CStartMgr::_evtReliveFormMouseEvent (~str 785) function

	
		C++:
	
	
	
		
```
else if (name == "btnReSpot")
{
 // We send a request for resurrection at the place of death
 CS_DieReturn(enumEPLAYER_RELIVE_ITEM_ORIGIN);
```


---

### Reply #2
**Lullz** — 2026-03-26

Nice idea.

IMO, there should be a way to counter it: a skill that force a dead player to respawn in town.


---

### Reply #3
**zLuke** — 2026-03-26

On the server, in CCharacter::Cmd_BeginSkill(...), there is a strict check if (!IsLiveing() || ...) return; — it disables any active use of skills for a dead character. Of course, you can rewrite this check and allow the casting of a specific skill for self-resurrection. 

However, in my opinion, my implementation is consistent with most MMORPGs, such as World of Warcraft, Perfect World, Lineage II, Lost Ark, etc. 

Additionally, this implementation allows you to profitably sell resurrection items for IMPs. ![;)](https://cdn.jsdelivr.net/joypixels/assets/8.0/png/unicode/64/1f609.png)


---

### Reply #4
**Lullz** — 2026-03-26

Sorry for the confusion, but what I meant is that enemies should be able to counter resurrection mechanics.

For example:

- Player 1 dies and is waiting for the resurrection cooldown.

- Player 2 can cast a skill on Player 1’s corpse to force them to respawn in town.


---

### Reply #5
**zLuke** — 2026-03-26

> 
	
		
			
				[Lullz said:](/goto/post?id=430)
			
		
	
	
		
		
		
			Sorry for the confusion, but what I meant is that enemies should be able to counter resurrection mechanics.

For example:

- Player 1 dies and is waiting for the resurrection cooldown.

- Player 2 can cast a skill on Player 1’s corpse to force them to respawn in town.
		
		
		Click to expand...


---

### Reply #6
**zLuke** — 2026-03-26

![zLuke](/data/avatars/s/0/81.jpg?1771721305)
	
	
		
			
				Source Development
			
			[Thread 'Banish Soul'](/threads/banish-soul.160/)
		

		
			Mar 26, 2026


---

### Reply #7
**ikaro** — 2026-04-10

Amazing idea! It would be interesting to use a Lua Plugin to remove this functionality in the final minutes of a given maze, preventing some joker from trying to respawn in the last seconds of the map to receive a certain reward.


---

### Reply #8
**zLuke** — 2026-04-10

> 
	
		
			
				[ikaro said:](/goto/post?id=493)
			
		
	
	
		
		
		
			Amazing idea! It would be interesting to use a Lua Plugin to remove this functionality in the final minutes of a given maze, preventing some joker from trying to respawn in the last seconds of the map to receive a certain reward.
		
		
		Click to expand...


---

### Reply #9
**ikaro** — 2026-04-10

> 
	
		
			
				[zLuke said:](/goto/post?id=494)
			
		
	
	
		
		
		
			In the lua script, you can completely disable resurrection on certain maps.

	
		C++:
	
	
	
		
```
-- List of maps where resurrection at the place of death is prohibited
local FORBIDDEN_RESURRECT_MAPS = {
 "guildwar",
 -- Add other maps as needed.
 -- "map_name_2",
 -- "map_name_3",
}
```
