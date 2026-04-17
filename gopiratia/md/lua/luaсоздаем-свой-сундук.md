# [Lua]Создаем свой сундук

**URL:** https://go-piratia.ru/topic/141-lua%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%B5%D0%BC-%D1%81%D0%B2%D0%BE%D0%B9-%D1%81%D1%83%D0%BD%D0%B4%D1%83%D0%BA/
**Posts:** 3

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-11-04

Пример сундука с аппарелями

function zodiac_aries ( role , Item )
	 local Item_CanGet = GetChaFreeBagGridNum ( role )
	 if Item_CanGet < 4 then
		SystemNotice(role ,"To open a Aries Apparel Chest requires at least 4 empty inventory slots")
		UseItemFailed ( role )
		return
	end
	local cha_type = GetChaTypeID ( role ) -- GetRace
	if cha_type == 1 then --Lance
	 GiveItem ( role , 0 , 5341 , 1 , 4 )
	 GiveItem ( role , 0 , 5342 , 1 , 4 )
	 GiveItem ( role , 0 , 5343 , 1 , 4 )
	elseif cha_type == 2 then -- Carsise
	 GiveItem ( role , 0 , 5345 , 1 , 4 )
	 GiveItem ( role , 0 , 5346 , 1 , 4 )
	 GiveItem ( role , 0 , 5347 , 1 , 4 )
	elseif cha_type == 3 then --Phyllis
	 GiveItem ( role , 0 , 5349 , 1 , 4 )
	 GiveItem ( role , 0 , 5350 , 1 , 4 )
	 GiveItem ( role , 0 , 5351 , 1 , 4 )
	elseif cha_type == 4 then --Ami
	 GiveItem ( role , 0 , 5352 , 1 , 4 )
	 GiveItem ( role , 0 , 5353 , 1 , 4 )
	 GiveItem ( role , 0 , 5354 , 1 , 4 )
	 GiveItem ( role , 0 , 5355 , 1 , 4 )
	end
end

	 

	Пример сундука с случайной наградой

function Random_Item ( role , Item )
	 local Item_CanGet = GetChaFreeBagGridNum ( role )
	 if Item_CanGet < 1 then
		SystemNotice(role ,"To open a Random Chest requires at least 1 empty inventory slots")
		UseItemFailed ( role )
		return
	end

	local rand = math.random(1,3)

	if rand == 1 then 
		GiveItem ( role , 0 , 7555 , 1 , 4)
	end
	
	if rand == 2 then
		GiveItem ( role , 0 , 7556 , 1 , 4)
	end
	
	if rand == 3 then
		GiveItem ( role , 0 , 7557 , 1 , 4)
	end
end

	 

	Более интересный пример создания сундука с случайной наградой

function ItemUse_RandomItemChest ( role , Item ) ---------- Random item chest
 local Cha_Boat = GetCtrlBoat ( role )
 if Cha_Boat ~= nil then
 SystemNotice( role , "Cannot use while sailing" )
 UseItemFailed ( role )
 return
 end
 
 local Item_CanGet = GetChaFreeBagGridNum ( role )
 if Item_CanGet < 2 then
 SystemNotice(role ,"You don't have enough slots")
 UseItemFailed ( role )
 return
 end
 
	-- Giving random item's when opening Chest, list them below
	local Item = {}
		Item[1] = 2792 -- Flash Bomb Lv5
		Item[2] = 2794 -- Soul Detector Lv5
		Item[3] = 1860 -- Blessed Potion
 
	-- The range is (1,3) at the moment, if you add more like 10 item, make it (1,10) so counts random for that and so on
	local i = math.random(1,Item.n) -- <-- range for the above item
	GiveItem(role,0,Item[i],1,4)
end


---

### Reply #1
**MoonBox** — 2025-10-09

Вот ещё интересный вариант, с ключом (Пурпурный сундук)

	 

	
		function ItemUse_TestCest1 (role, Item)
	
	 

	
		    local Cha_Boat = GetCtrlBoat ( role )
	

	
		    if Cha_Boat ~=  nil then
	

	
		        SystemNotice( role , "Нельзя использовать в море!" )
	

	
		        UseItemFailed ( role )
	

	
		        return
	

	
		    end
	

	
		    local Item_CanGet = GetChaFreeBagGridNum ( role )   
	

	
		     if Item_CanGet < 1 then
	

	
		        SystemNotice(role ,"Недостаточно места в инвентаре")
	

	
		        UseItemFailed ( role )
	

	
		        return
	

	
		    end
	

	
		    local i= CheckBagItem( role, 7101 )  --ID ключа
	

	
		    if i <=0 then
	

	
		        SystemNotice(  role , "Нужен ключ соответствующего цвета!")
	

	
		        UseItemFailed ( role )
	

	
		        return LUA_FALSE
	

	
		    end
	

	
		    
	

	
		    local s = DelBagItem ( role , 7101 , 1 ) --ID ключа
	

	
		    local   sc = math.random(1,100)
	

	
		    local itemname = ""
	

	
		    if  sc <=50 then    
	

	
		        GiveItem ( role , 0 , 7114 , 1 , 4 )
	

	
		        itemname = "Зеленый сундук"
	

	
		    elseif sc <=65 then     
	

	
		        GiveItem ( role , 0 , 7102 , 1 , 4 )
	

	
		        itemname = "Зеленый ключ"
	

	
		    elseif sc <=80 then
	

	
		        GiveItem ( role , 0 , 7085 , 5 , 4 )
	

	
		        itemname = "Загадочная коробка"
	

	
		    elseif sc <=95 then
	

	
		        GiveItem ( role , 0 , 7084 , 5 , 4 )
	

	
		        itemname = "Сундук королевы феи"
	

	
		    else   
	

	
		        GiveItem ( role , 0 , 7099 , 3 , 4 )
	

	
		        itemname = "Пиастра"
	

	
		    end
	

	
		    local cha_name = GetChaDefaultName ( role )
	

	
		    Notice ( "Игрок" ..cha_name.." открыл Пурпурный сундук и получил "..itemname )
	

	
		end
	

			
				

	**Edited October 9, 2025 by MoonBox**


---

### Reply #2
**MoonBox** — 2025-10-11

Пример сундука с 3 ключами.

	 

	
		function ItemUse_LockedChest1 (role, Item)
