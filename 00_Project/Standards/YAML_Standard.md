# YAML Standard

## Purpose

YAML используется как машинно-читаемая шапка файла.

Она нужна для:

- поиска;
    
- фильтрации;
    
- Dataview-запросов;
    
- связей между объектами;
    
- контроля статуса информации.
    

YAML находится в начале `.md` файла:

```yaml
---
type:
status:
data_layer:
source:
tags:
---
```

---

# Required Fields

Каждый объект должен иметь поля:

```yaml
---
type:
status:
data_layer:
source:
tags:
---
```

---

## type

Тип объекта.

Допустимые значения описаны в:

```text
00_Project/Standards/Object_Model.md
```

Примеры:

```yaml
type: creature
type: relic
type: character
type: layer
type: phenomenon
type: session
type: consequence
```

---

## status

Статус информации.

```yaml
status: canon
status: derived
status: adaptation
status: homebrew
status: campaign
status: draft
```

---

## data_layer

Слой данных проекта.

```yaml
data_layer: canon
data_layer: adaptation
data_layer: campaign
```

---

## source

Источник информации.

```yaml
source:
  - manga
  - anime
  - movie
  - guidebook
  - wiki
  - adaptation
  - homebrew
  - campaign
```

---

## tags

Теги для быстрого поиска.

```yaml
tags:
  - abyss
  - layer_1
  - relic
```

Теги пишем маленькими буквами через `_`.

---

# Recommended Fields

Эти поля добавляются, если они полезны.

---

## aliases

Альтернативные названия.

```yaml
aliases:
  - Sovereign of Dawn
  - Lord of Dawn
```

---

## layers

Связанные слои Бездны.

```yaml
layers:
  - Layer_1
  - Layer_2
```

---

## related

Связанные объекты.

```yaml
related:
  - Abyss
  - Bondrewd
  - Prushka
```

---

## location

Место, с которым связан объект.

```yaml
location:
  - Orth
  - Ido_Front
```

---

## affiliation

Организация или группа.

```yaml
affiliation:
  - Delvers_Guild
  - Umbra_Hands
```

---

## campaign

Кампания, к которой относится объект.

```yaml
campaign:
  - Campaign_001
```

Используется только для `data_layer: campaign`.

---

## session

Игровая сессия, к которой относится объект.

```yaml
session:
  - Session_001
```

---

## created

Дата создания файла.

```yaml
created: 2026-06-19
```

---

## updated

Дата последнего значимого изменения.

```yaml
updated: 2026-06-19
```

---

# Naming Rules

## File Names

Файлы называем на английском.

Правильно:

```text
Bondrewd.md
Curse_of_the_Abyss.md
Layer_1.md
Orb_Piercer.md
```

Неправильно:

```text
Бондруд.md
Проклятие_Бездны.md
```

---

## Object References

В YAML указываем имя файла без `.md`.

```yaml
related:
  - Bondrewd
  - Curse_of_the_Abyss
```

---

# Minimalism Rule

YAML не должен превращаться в анкету на 50 полей.

В YAML храним только то, что нужно для:

- поиска;
    
- Dataview;
    
- связей;
    
- фильтрации;
    
- сортировки.
    

Всё остальное пишем обычным Markdown-текстом.

---

# Example

```markdown
---
type: creature
status: canon
data_layer: canon
source:
  - manga
  - anime
tags:
  - abyss
  - creature
  - predator
layers:
  - Layer_1
related:
  - Abyss
created: 2026-06-19
updated: 2026-06-19
---

# Corpse Weeper

## Summary

Описание существа...

## Canon Notes

Каноническая информация...

## Game Notes

Игровые заметки...
```