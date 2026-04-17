# [Fix]Ограничение во времени на продажу предметов

**URL:** https://go-piratia.ru/topic/111-fix%D0%BE%D0%B3%D1%80%D0%B0%D0%BD%D0%B8%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B2%D0%BE-%D0%B2%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%B8-%D0%BD%D0%B0-%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%B6%D1%83-%D0%BF%D1%80%D0%B5%D0%B4%D0%BC%D0%B5%D1%82%D0%BE%D0%B2/
**Posts:** 3

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-10-30

Открываем **npcsdk**.**lua**Ищем function **Buy **и заменяем все на это

function Buy( character, npc, trade, itemtype, index1, index2, count )
local antibuy = GetChaStateLv ( character , 5 )
if antibuy == 0 then
PRINT( "Buy" )
itemtype = itemtype + 1
index1 = index1 + 1
if trade[itemtype] == nil or trade[itemtype].item == nil or trade[itemtype].item[index1] == nil then
PRINT( "Buy: Function error." )
SystemNotice( character, "Buy: Функция ошибочна. " )
return LUA_FALSE
end
local itemid = trade[itemtype].item[index1]
local statelv = 1
local statetime = 3 --Задержка (в секундах)
	 SafeBuy( character, itemid, index2, count )
AddState ( character, character, 5, statelv, statetime )
return LUA_TRUE
else
SystemNotice(character, "Покупать можно каждые 3 секунды. ")
return LUA_FALSE
end
end

	Чуть выше находим function **sale **и также все заменяем

function Sale( character, npc, index, count )
local antisale = GetChaStateLv ( character , 5 )
if antisale == 0 then
PRINT( "Sale" )
if index == nil or count == nil then
PRINT( "Sale:Function parameter error!" )
SystemNotice( character, "Sale: Функция ошибочна. " )
return LUA_FALSE
end
local statelv = 1
local statetime = 3 --Задержка (в секундах)
	 SafeSale( character, index, count )
AddState ( character, character, 5, statelv, statetime )
return LUA_TRUE
else
SystemNotice(character, "Продавать можно каждые 3 секунды. ")
return LUA_FALSE
end
end


---

### Reply #1
**EnKit** — 2024-01-17

А можете подсказать, как наоборот убрать это ограничение? Просто удалить всё что написано выше или нужно подчищать что-то конкретное?)


---

### Reply #2
**Go-piratia** — 2024-01-18

Необходимо убрать проверку  и назначение state. 

if antibuy == 0 then

AddState ( character, character, 5, statelv, statetime )

	Важно сохранить логическую целостность алгоритма.
