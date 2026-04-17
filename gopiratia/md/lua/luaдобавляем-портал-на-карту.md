# [Lua]Добавляем портал на карту

**URL:** https://go-piratia.ru/topic/110-lua%D0%B4%D0%BE%D0%B1%D0%B0%D0%B2%D0%BB%D1%8F%D0%B5%D0%BC-%D0%BF%D0%BE%D1%80%D1%82%D0%B0%D0%BB-%D0%BD%D0%B0-%D0%BA%D0%B0%D1%80%D1%82%D1%83/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-10-30

**Портал карты(динамичный)**
	 

	Идём: **Сервер/resource/карта/ctrl.lua**Видим:

function get_map_entry_pos_garner2() --

local POS_X=Координаты
local POS_Y=Координаты
return POS_X , POS_Y

end

function init_entry(map)

SetMapEntryMapName(map, "карта") --
SetMapEntryTime(map, "2006/10/18/14/0", "0/6/0", "0/0/сколько открыт порт", "0/0/сколько открыта карта") --

end

	Например для хаоса:

function get_map_entry_pos_garner2() -- координаты

local POS_X=1370
local POS_Y=532
return POS_X , POS_Y

end

function init_entry(map)

SetMapEntryMapName(map, "darkblue") -- карта - ледынь
SetMapEntryTime(map, "2006/10/18/14/0", "0/6/0", "0/0/30", "0/0/45") -- карта открывается на 45 минут (тп есть 30 минут)

end

	А теперь идём в файл entry.lua** и функции begin_enter_карта меняем:

function begin_enter_карта(role, copy_mgr)
        MoveCity(role, "Название из ScriptDefine.lua")

	 

	
**Название портала**Идём: **Сервер/resource/карта/entry.lua**Видим:

function after_create_entry(entry)
local copy_mgr = GetMapEntryCopyObj(entry, 0) --
local EntryName = "Надпись над тп"
SetMapEntryEventName( entry, EntryName )

	 

	**Портал между картами(статичный)**

	Идём:** Сервер\resource\magicsea\magicseaswhmap.txt** (для залива сокровищ)Видим:

5 2492 4 87711,375611 -1 jialebi 73411,103211 1 Magical Ocean - Caribbean

	Переносим в строчку в (например): **Сервер\resource\garner\garnerswhmap.txt** (для аскарона) при этом меняя координаты. Удачи
