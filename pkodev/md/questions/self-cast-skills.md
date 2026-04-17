# cast skills

**Category:** Self
**URL:** https://pkodev.com/threads/self-cast-skills.173/
**Posts:** 6

---

## Original Post
**Author:** Lullz  
**Date:** 2026-04-16

Hello,

Is it possible to use keyboard shortcuts (F1–F12, etc.) to self-cast skills (heal, buffs, recovery)?

The idea is to allow Cleric/SM players to use support skills on themselves more quickly, without having to click on their character or the UI.

Thank you !


---

### Reply #1
**zLuke** — 2026-04-16

This is set by the chApplyTarget field (in skillinfo.txt, Process target column 18).

The chApplyTarget specifies values from

	
		C++:
	
	
	
		
```
enum ESkillObjType
{
 // Main skill target type:
 // 1 - self, 2 - team, 3 - scene/ground point, 4 - enemy, 5 - any target.

 enumSKILL_TYPE_SELF = 1, // Self
 enumSKILL_TYPE_TEAM = 2, // Teammate / party member
 enumSKILL_TYPE_SCENE = 3, // Ground point (area target)
 enumSKILL_TYPE_ENEMY = 4, // Hostile target
 enumSKILL_TYPE_ALL = 5, // Any target
 enumSKILL_TYPE_PLAYER_DIE = 6, // Dead player (resurrection target)
 enumSKILL_TYPE_EXCEPT_SELF = 7, // Any target except self

 // Special targets (profession/interactive objects):
 enumSKILL_TYPE_REPAIR = 17, // Repairable object
 enumSKILL_TYPE_TREE = 18, // Tree
 enumSKILL_TYPE_MINE = 19, // Ore vein
 enumSKILL_TYPE_TRADE = 22, // Trade object
 enumSKILL_TYPE_FISH = 28, // Fishing spot
 enumSKILL_TYPE_SALVAGE = 29, // Salvage object
};
```


---

### Reply #2
**Lullz** — 2026-04-16

Thank you Luke for your response,

But what I meant was more tricky:

- No change in skills

- Tweaking the client to add a shortcut for self-casting, 

- Still allowing the same skill to be cast on other players (using another shortcut).

Example:

Skill: Heal

F1: Heal by selecting a target

F2: Seal-heal (without selecting a target)


---

### Reply #3
**zLuke** — 2026-04-16

After making these changes to the client code, the skills defined in IsRightClickSelfCastSkill will be cast on your character when you right-click on the quick access panel. The behavior of the left mouse button will not change, and you will be able to apply buffs to other characters.


---

### Reply #4
**Lullz** — 2026-04-16

That's awesome !

Is it possible to do it using keyboard shortcut ?

Maybe by configuring a keybind to be a self-cast shortcut


---

### Reply #5
**zLuke** — 2026-04-16

To be honest, I haven't delved into this yet. In the future, I plan to modify the quick key system by customizing shortcuts, but I haven't reached that point yet.
