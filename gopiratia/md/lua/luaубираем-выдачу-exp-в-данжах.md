# [Lua]Убираем выдачу exp в данжах

**URL:** https://go-piratia.ru/topic/112-lua%D1%83%D0%B1%D0%B8%D1%80%D0%B0%D0%B5%D0%BC-%D0%B2%D1%8B%D0%B4%D0%B0%D1%87%D1%83-exp-%D0%B2-%D0%B4%D0%B0%D0%BD%D0%B6%D0%B0%D1%85/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-10-30

variable.lua:

MapExpZero = {}
MapExpZero["Карта"] = true
MapExpZero["Карта2"] = true
MapExpZero["Карта3"] = true

	exp_and_level.lua:Находим функцию:

function ShareTeamExp ( dead , team_atker , dead_exp , The_Killer)

	И в ней находим строчку:

exp = exp + exp_up

	К ней добавляем:

exp = exp + exp_up* zero_exp

	Затем выше этой строчки добавим код:

zero_exp = 1
local map_name = GetChaMapName (TurnToCha(t[i]) )
if(MapExpZero[map_name] ~= nil)then
 zero_exp = 0
end

	В итоге у Вас должно получиться так:

zero_exp = 1
local map_name = GetChaMapName (TurnToCha(t[i]) )
if(MapExpZero[map_name] ~= nil)then
 zero_exp = 0
end
exp = exp + exp_up* zero_exp
