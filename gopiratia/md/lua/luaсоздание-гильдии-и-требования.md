# [Lua]Создание гильдии и требования

**URL:** https://go-piratia.ru/topic/119-lua%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B3%D0%B8%D0%BB%D1%8C%D0%B4%D0%B8%D0%B8-%D0%B8-%D1%82%D1%80%D0%B5%D0%B1%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-10-30

**Функции для изучения логики создания**(Используйте поиск по сборке):

-- Проверки на создание гильдии 
function AskGuildItem(role, Guild_type)

end

-- Проверка наличия предметов в инвентаре
function Check_BagItem(role, a, b)

end

-- Функция создания гильдии вызывается из C++
function DeductGuildItem(role, Guild_type)
end

-- Запрос на вступление в гильдию
function AskJoinGuild(role, guild_type)

end

	 

	**Таблица с требованиями**(Используйте поиск по сборке):

--------------------------------------------------------
-- Массив с условиями для создания гильдии NAVY --
--------------------------------------------------------
Guild1_ItemMax = 1 -- Количество (в общем и целом) предметов, необходимых для создания гильдии
Guild1_item = {}
Guild1_count = {}

Guild1_fame = 0
Guild1_Gold = 100000 -- Кол-во денег необходимое для создания гильдии
Guild1_item[1] = 1780
Guild1_count[1] = 1 -- Первый столбец: Камень клятвы (ID 1780) Второй столбец: Кол-во предметов
Guild1_item[2] = -1
Guild1_count[2] = -1
Guild1_item[3] = -1
Guild1_count[3] = -1
Guild1_item[4] = -1
Guild1_count[4] = -1
Guild1_item[5] = -1
Guild1_count[5] = -1

--------------------------------------------------------
-- Массив с условиями для создания гильдии PIRATE --
--------------------------------------------------------
Guild2_ItemMax = 1
Guild2_item = {} -- Количество (в общем и целом) предметов, необходимых для создания гильдии
Guild2_count = {}

Guild2_fame = 0
Guild2_Gold = 100000 -- Кол-во денег необходимое для создания гильдии
Guild2_item[1] = 1780
Guild2_count[1] = 1 -- Первый столбец: Камень клятвы (ID 1780) Второй столбец: Кол-во предметов
Guild2_item[2] = -1
Guild2_count[2] = -1
Guild2_item[3] = -1
Guild2_count[3] = -1
Guild2_item[4] = -1
Guild2_count[4] = -1
Guild2_item[5] = -1
Guild2_count[5] = -1

JOINGUILD_NAVY_FAME = 0
JOINGUILD_PIRATE_FAME = 0
