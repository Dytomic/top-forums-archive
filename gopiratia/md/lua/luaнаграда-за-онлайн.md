# [Lua]Награда за онлайн

**URL:** https://go-piratia.ru/topic/114-lua%D0%BD%D0%B0%D0%B3%D1%80%D0%B0%D0%B4%D0%B0-%D0%B7%D0%B0-%D0%BE%D0%BD%D0%BB%D0%B0%D0%B9%D0%BD/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-10-30

Данный скрипт дает награду спустя определенное время. Если персонаж выйдет из игры, то время сброситься. Вам не придется перезагружать сервер, достаточно лишь ввести команду, чтобы включить скрипт.Как это работает?**Игрок должен быть 75и выше уровня, и быть онлайн в течение 24 часов без выход из игры.Откройте functions.lua** и добавьте скрипт в cha_timer**:

local SetHours = 24 -- Время, через которое выдается вещь
local Level = GetChaAttr( role , ATTR_LV )
if OnlineEvent == true and math.mod(now_tick, SetHours*3600) == 0 and now_tick > 0 and Level > 75 then
local Prize = {}
-- Призы
Prize[1] = 192 -- Сундук Килин
Prize[2] = 2843 -- Законный сундук Черного дракона
Prize[3] = 2842 -- Скелет Смерти
local i = math.random (1,3) -- Рандом (1 из 3)

-- Получаем приз
local cha = TurnToCha (role)
local ItemName = GetItemName (Prize[i])
GiveItem ( cha , 0 , Prize[i] , 1 , 4 )

-- Отправляем уведомление игроку
SystemNotice(cha,"Поздравляем! Вы находитесь онлайн ".. SetHours .." часов, и вы были награждены ".. ItemName .."! #10")
end

	Откройте variable.lua** и добавьте это в конце:

OnlineEvent = false

	Сделали? Теперь как их использовать!Для активации вводим в местный чат:**

&lua_all OnlineEvent = true

	Для выключения вводим:**

&lua_all OnlineEvent = false
