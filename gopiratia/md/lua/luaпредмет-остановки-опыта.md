# [Lua]Предмет остановки опыта

**URL:** https://go-piratia.ru/topic/149-lua%D0%BF%D1%80%D0%B5%D0%B4%D0%BC%D0%B5%D1%82-%D0%BE%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B8-%D0%BE%D0%BF%D1%8B%D1%82%D0%B0/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-11-04

В **iteminfo**.**txt **добавляем 

xxxx Остановка опыта n0539 10130005 0 0 0 0 0 0 41 0 0 0 0 0 1 1 1 1 99 0 84 -1,-2,-2,-2 0 -1,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2,-2 0 0 -1,-2,-2,-2,-2,-2,-2,-2,-2,-2 -1,-2,-2,-2,-2,-2,-2,-2,-2,-2 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0 0,0 0,0 0 0 0 0 0 0 0 0 0 0 0 0 0 0,0 0,0 0,0 You wont gain any exp from any mobs with me in your inventory :) 0

	В файле **resource/scripts/calculate/exp_and_level.lua **ищем **exp_up = exp_up * EXP_RAID_STATE ** и выше или ниже добавляем:

local checkstone = CheckBagItem( TurnToCha(t[i]), XXXX ) -- ID из Iteminfo.txt 
if checkstone > 0 then
	exp_up = 0
	SystemNotice ( TurnToCha(t[i]) , "No EXP Stone activated! You obtained no exp from this mob" )
end

	 

	Теперь если этот предмет находится в инвентаре персонаж не будет получать опыт
