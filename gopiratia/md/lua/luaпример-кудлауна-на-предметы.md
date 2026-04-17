# [Lua]Пример кудлауна на предметы

**URL:** https://go-piratia.ru/topic/148-lua%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D0%BA%D1%83%D0%B4%D0%BB%D0%B0%D1%83%D0%BD%D0%B0-%D0%BD%D0%B0-%D0%BF%D1%80%D0%B5%D0%B4%D0%BC%D0%B5%D1%82%D1%8B/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-11-04

Скрипт устанавливает кулдаун на использование предмета.  Добавляем в **ItemEffect**.**lua**

Gyosa = {}
function ItemUse_SSSJ ( role , Item )
 local name = GetChaDefaultName(role)
 if Gyosa[name] == nil then
 Gyosa[name] = { UsedTime = os.time() }
 end
 
 local cooldown = Gyosa[name].UsedTime - os.time()
 if cooldown > 0 then
 SystemNotice(role,"Gyoza cooldown on effect wait "..cooldown.." second(s) to use again!")
 UseItemFailed(role)
 return
 end
 
 mxhp = GetChaAttr(role,ATTR_MXHP)
 hp_resume = mxhp * 0.3
 hp = hp + hp_resume
 
 if hp > mxhp then
 hp = mxhp
 end
 SetCharaAttr(hp, role, ATTR_HP)
 Gyosa[name].UsedTime = os.time()+10
end
