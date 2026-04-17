# [Lua]Предмет дающий баф

**URL:** https://go-piratia.ru/topic/143-lua%D0%BF%D1%80%D0%B5%D0%B4%D0%BC%D0%B5%D1%82-%D0%B4%D0%B0%D1%8E%D1%89%D0%B8%D0%B9-%D0%B1%D0%B0%D1%84/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-11-04

В **iteminfo**.**txt **добавляем (не забываем ставить табуляцию)

7000	Buff Ticket	n1481	10130001	0	0	0	0	0	00	31	0	0	0	0	0	1	1	1	1	99	0	200	-1	0	-1 0 0 -1 -1 0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0,0 0 0,0 0,0 0 0 0 0 0 0 0 0 0 ItemUse_buffticket 0 0 0 0 0 0 Double click to get all buffs in 5 minutes.

	 

	В **ItemEffect**.**lua **добавляем функцию предмета:

function ItemUse_buffticket( role , Item )
 local Cha_Boat = GetCtrlBoat(role)

 if Cha_Boat ~= nil then
 SystemNotice(role , "Not usable on the sea." )
 UseItemFailed (role)
 return
 end
 
 local buff1 = GetChaStateLv(role,STATE_SHPF) -- STATE_SHPF идентификатор из skilleff.txt
 local buff2 = GetChaStateLv(role,STATE_XLZH) -- STATE_XLZH идентификатор из skilleff.txt
 local buff3 = GetChaStateLv(role,STATE_TSHD) -- STATE_TSHD идентификатор из skilleff.txt
 local buff4 = GetChaStateLv(role,STATE_FZLZ) -- STATE_FZLZ идентификатор из skilleff.txt
 local buff5 = GetChaStateLv(role,STATE_MLCH) -- STATE_MLCH идентификатор из skilleff.txt
 
 if buff1 >= 1 or buff2 >= 1 or buff3 >= 1 or buff4 >= 1 or buff5 >= 1 then
 SystemNotice(role,"Only you can use this ticket after duration of buffs end.")
 UseItemFailed(role)
 return
 end

 local del_item = DelBagItem( role , 7000 , 1 )
 if del_item == 1 then
 AddState ( role , role , STATE_SHPF , 10 , 600 ) -- STATE_SHPF идентификатор из skilleff.txt, 10 - уровень бафа, 600 время в секундах 
 AddState ( role , role , STATE_XLZH , 10 , 600 )
 AddState ( role , role , STATE_TSHD , 10 , 600 )
 AddState ( role , role , STATE_FZLZ , 10 , 600 )
 AddState ( role , role , STATE_MLCH , 10 , 600 )
 BickerNotice( role , "You recived Harden, Spiritual Fire, Tempest Bolt, Angelic Shield, Intense Magic for 5 minutes!" )
 end
end
