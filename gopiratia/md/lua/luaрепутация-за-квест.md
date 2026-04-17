# [Lua]Репутация за квест

**URL:** https://go-piratia.ru/topic/140-lua%D1%80%D0%B5%D0%BF%D1%83%D1%82%D0%B0%D1%86%D0%B8%D1%8F-%D0%B7%D0%B0-%D0%BA%D0%B2%D0%B5%D1%81%D1%82/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-11-04

Создаем функцию в **function**.**lua **

function AddReputation(role,amount)
 local playerReputation = GetChaAttr(role, ATTR_FAME)
 playerReputation = playerReputation + amount
 SetCharaAttr(playerReputation, role, ATTR_FAME)
 SystemNotice(role,"You've recieved "..amount.." reputation! ["..playerReputation.."]")
end

	В **MissionSdk**.lua находим блок похожий c **elseif actions*.func ==**** и добавляем свое условие. 
*
*

*
elseif actions[i].func == AddReputation then
 PRINT( "ActionProc:AddReputation, p1 = ", actions[i].p1 )
 AddReputation( character, actions[i].p1 )*

*
*
	В самом задании используем следующим образом
*
*

*
MisResultAction(AddReputation,1000) -- Give 1k rep*

*
*
	 
*
*
*
