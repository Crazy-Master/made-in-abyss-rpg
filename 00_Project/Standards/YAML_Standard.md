# YAML Standard

## Назначение

YAML используется для хранения структурированной информации об объектах мира.

YAML располагается в начале файла между разделителями:

```yaml
---
...
---
```

Основное описание объекта размещается ниже в обычном Markdown.

---

## Общие правила

### Используем только английские идентификаторы

Правильно:

```yaml
type: creature
```

Неправильно:

```yaml
type: существо
```

---

### Названия файлов

Используем:

```text
Bondrewd.md
Corpse_Weeper.md
Layer_1.md
Star_Compass.md
```

Не используем:

```text
Бондруд.md
Трупный_ревун.md
```

Русский язык допускается только внутри описания статьи.

---

### Ссылки на другие объекты

Используем имя файла без расширения.

Пример:

```yaml
related:
  - Bondrewd
  - Prushka
```

---

## Обязательные поля

Каждый объект должен содержать:

```yaml
---
type:
status:
source:
tags:
---
```

---

## type

Тип объекта.

Допустимые значения:

```yaml
type: creature
type: relic
type: character
type: location
type: layer
type: faction
type: event
type: flora
type: phenomenon
```

---

## status

Статус информации.

Допустимые значения:

```yaml
status: canon
status: derived
status: adaptation
status: homebrew
status: draft
```

---

## source

Источник информации.

Пример:

```yaml
source:
  - manga
  - anime
```

Допустимые значения:

```yaml
manga
anime
movie
guidebook
wiki
adaptation
homebrew
```

---

## tags

Ключевые теги.

Пример:

```yaml
tags:
  - abyss
  - predator
  - layer_1
```

---

## Необязательные поля

Используются при необходимости.

---

### related

Связанные объекты.

```yaml
related:
  - Bondrewd
  - Nanachi
```

---

### layer

Связанные слои Бездны.

```yaml
layer:
  - Layer_1
  - Layer_2
```

---

### affiliation

Принадлежность к организации.

```yaml
affiliation:
  - Delvers_Guild
```

---

### aliases

Альтернативные названия.

```yaml
aliases:
  - Sovereign of Dawn
```

---

## Принцип минимализма

Не добавлять поле в YAML только потому, что это возможно.

Если информация используется только в описании статьи — она должна находиться в Markdown.

YAML хранит только данные, полезные для поиска, фильтрации и связей между объектами.