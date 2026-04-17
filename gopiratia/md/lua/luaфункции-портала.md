# [Lua]Функции портала

**URL:** https://go-piratia.ru/topic/128-lua%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B8-%D0%BF%D0%BE%D1%80%D1%82%D0%B0%D0%BB%D0%B0/
**Posts:** 1

---

## Original Post
**Author:** Go-piratia  
**Date:** 2023-10-31

Данные функции должны быть прописаны для каждой карты, в которую есть **портал **в файлах **entry**.**lua. **Для примера взята карта **darkswamp: **

function config_entry(entry)
	SetMapEntryEntiID(entry, 193, 1) -- наземный портал
end

-- Вызывается каждый раз когда создается портал
function after_create_entry(entry)
end

-- Вызывается каждый раз когда закрывается портал
function after_destroy_entry_darkswamp(entry)
end

-- Вызывается каждый раз когда игрок заходит в игру
function after_player_login_darkswamp(entry, role)
end

-- Проверка может ли персонаж зайти, вызывается каждый раз при попытке входа (инициализируется 1 раз при инициализации карты) и имеет ограничение на кол-во условий.
function check_can_enter_darkswamp(role, copy_mgr)
	return 1
end

-- Вызывается каждый раз когда персонаж заходит в портал после проверки
function begin_enter_darkswamp(role, copy_mgr)
end
