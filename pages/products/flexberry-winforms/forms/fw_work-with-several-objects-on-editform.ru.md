---
title: Работа на форме редактирования с полями нескольких объектов 
sidebar: flexberry-winforms_sidebar
keywords: View (представление)
toc: true
permalink: ru/fw_work-with-several-objects-on-editform.html
folder: products/flexberry-winforms/
lang: ru
---
Иногда встаёт задача организовать работу с полями объектов разных классов на одной форме редактирования. Например, необходима форма для быстрого ввода, где часть полей принадлежит одному классу, часть - другому и т.д. В таком случае необходимо отслеживать сохранение этого "сложного представления".

## Вариант решения через EditManager
Одним из вариантов решения поставленной задачи может быть использование нескольких [EditManager](fw_editmanager.html)'ов.

### Привязка EditManager
В статье [Как редактировать объекты данных на формах, связывание полей ввода со свойствами объекта данных](fw_edit-data-objects-on-forms.html) описано, как создать и привязать [EditManager](fw_editmanager.html)'ы к объектам.

### Сохранение объектов
Логика сохранения объектов из "сложного представления" зависит от конкретной задачи (например, по каким полям определять, что такой же объект уже есть в базе, как интерпретировать изменение сохранённого объекта и прочее).
При сохранении "сложного представления" необходимо обратить внимание на моменты, отмеченные в статьях:
* [Обработка множества объектов (в т.ч. и разнотипных)](fo_processing-multiple-objects.html)
* [Обновление связанных объектов](fo_update-related-objects.html)

## Смотри также
* [Чтение принадлежащих различным классам объектов в одном представлении](fo_reading-several-types-objects.html)
* [Универсальная форма редактирования](fw_uni-win-edit.html)
* [Переключение редактируемого объекта без закрытия формы редактирования ](fw_switch-editing-object.html)