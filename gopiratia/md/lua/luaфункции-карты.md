# [Lua]Функции карты

**URL:** https://go-piratia.ru/topic/127-lua%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B8-%D0%BA%D0%B0%D1%80%D1%82%D1%8B/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-10-31

Данные функции должны быть представлены для всех карт использующихся в **GameServer***.**cfg **в файлах **ctrl**.**lua **для каждого экземпляра карты. Для примера взята карта **darkswamp:**

--Вызывается каждый раз при инициализации карты
function config(map)
end

--Вызывается каждый раз при инициализации карты и возвращает координаты портала
function get_map_entry_pos_darkswamp()
end

--Вызывается каждый раз при инициализации карты
function init_entry(map)
end

--Срабатывает каждый раз после входа на карту
function after_enter_darkswamp(role, map_copy)
end

--Вызывается каждый раз при первом запуске копии карты
function map_copy_first_run_darkswamp(map_copy)
end

--Срабатывает каждый раз после выхода с карты
function before_leave_darkswamp(role)
end

--Вызывается каждый раз при попытке открыть портал и запустить карту (раз в 3 сек)
function can_open_entry_darkswamp(map)
end

--Вызывается каждые 4-5 секунд для экземпляра карты(для всех копий)
function map_run_darkswamp(map)
end

--Вызывается каждую секунду для каждой копии карты
function map_copy_run_darkswamp(map_copy)
end

--Вызывается каждые 5 минут для каждой копии карты
function map_copy_run_special_darkswamp(map_copy)
end
