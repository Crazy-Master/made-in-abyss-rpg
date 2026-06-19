# Object Model

## Purpose

Этот документ описывает основные типы объектов в проекте MadeInAbyss_RPG.

Он нужен для того, чтобы все заметки, шаблоны, YAML-метаданные и Dataview-запросы использовали единые названия сущностей.

---

# Data Layers

## Canon

Каноническая информация из Made in Abyss.

Примеры:

- Abyss
    
- Orth
    
- Bondrewd
    
- Layer_5
    
- Star_Compass
    

Canon не изменяется игровыми событиями.

---

## Adaptation

Игровая адаптация канона.

Примеры:

- правила проклятия Бездны
    
- правила экспедиций
    
- таблицы травм
    
- игровые эффекты реликвий
    

Adaptation объясняет, как канон работает за игровым столом.

---

## Campaign

События конкретных партий и экспедиций.

Примеры:

- Campaign_001
    
- Expedition_003
    
- Session_014
    
- Player_Character_Ran
    
- Consequence_014
    

Campaign может менять состояние игрового мира, но не переписывает канон.

---

# Core Object Types

## phenomenon

Крупное явление или закон мира.

Примеры:

- Abyss
    
- Curse_of_the_Abyss
    
- Force_Field
    

---

## layer

Слой Бездны.

Примеры:

- Layer_1
    
- Layer_2
    
- Layer_5
    

---

## location

Конкретное место.

Примеры:

- Orth
    
- Seeker_Camp
    
- Ido_Front
    

---

## settlement

Населённый пункт, аванпост или база.

Примеры:

- Orth
    
- Nanachi_Hideout
    
- Ganja_Village
    

---

## creature

Живое существо, опасный организм или животное.

Примеры:

- Corpse_Weeper
    
- Orb_Piercer
    
- Crimson_Splitjaw
    

---

## flora

Растение, гриб, водоросль или иной неподвижный организм.

---

## relic

Реликвия или артефакт Бездны.

Примеры:

- Star_Compass
    
- Blaze_Reap
    
- Zoaholic
    

---

## character

Именованный персонаж.

Примеры:

- Riko
    
- Reg
    
- Nanachi
    
- Bondrewd
    

---

## faction

Организация, группа, орден, государственная или научная структура.

Примеры:

- Delvers_Guild
    
- Umbra_Hands
    
- Foreign_Delvers
    

---

## event

Историческое событие канона или игрового мира.

Примеры:

- Birthday_Death_Disease
    
- Bondrewd_Experiments
    
- Expedition_003_Disaster
    

---

## expedition

Конкретный поход в Бездну.

Может быть каноническим или игровым.

---

## session

Игровая сессия.

Используется только для кампаний.

---

## consequence

Последствие игровой сессии, которое меняет состояние мира.

Примеры:

- мост разрушен
    
- персонаж погиб
    
- найден новый проход
    
- реликвия утеряна
    
- поселение предупреждено об угрозе
    

---

# Status Values

## canon

Подтверждено каноном.

---

## derived

Логически выведено из канона.

---

## adaptation

Игровая адаптация канона.

---

## homebrew

Полностью авторское дополнение.

---

## campaign

Возникло в ходе игры.

---

## draft

Черновик.

---

# Rule of Separation

Канон, адаптация и кампании не должны смешиваться в одном объекте без явной причины.

Если канонический объект получает игровые последствия, они описываются отдельным объектом типа consequence или campaign_note, а не переписывают исходный canon-файл.

Пример:

Канон:

- 03_Abyss/Overview/Abyss.md
    

Кампания:

- 13_Sessions/Consequences/Consequence_001_Damaged_Route_To_Layer_2.md
    

---

# Future Expansion

Новые типы объектов можно добавлять только через обновление этого документа.

Это нужно, чтобы не появлялись случайные типы вроде:

- monster
    
- beast
    
- animal
    
- npc
    
- person
    

Вместо этого используются уже утверждённые типы:

- creature
    
- character
    
- faction