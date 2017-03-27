---
title: Обновление связанных объектов
sidebar: flexberry-orm_sidebar
keywords: Flexberry ORM, Public
toc: true
permalink: ru/fo_update-related-objects.html
folder: products/flexberry-orm/
lang: ru
---

Возможна ситуация, когда сохранение некоторого [объекта данных](fo_dataobject.html) может повлечь сохранение связанных с ним объектов, которые явно не были переданы на сохранение.

## Обновление детейловых объектов вместе с [шапкой](fd_key-concepts.html)

Если обновляется объект, имеющий [детейловые объекты](fo_detail-associations-and-their-properties.html), то те также обновляются, если это предполагает их [статус](fo_processing-status-and-condition-of-load-object-data-services.html).

## Обновление мастеровых объектов вместе с внутренним

Если изменён [мастеровой объект](fd_master-association.html), то при обновлении объекта внутреннего класса обновляется также мастеровой.



Вышеуказанные правила применяются ко всем объектам, находящимся в цепочке изменений. Т.е., например, если есть объект внутреннего класса, у которого есть мастеровой с детейлами, то обновляются все. Важно помнить только, что `попадают только измененные объекты`, т.е., [статус](fo_processing-status-and-condition-of-load-object-data-services.html) которых предполагает обновление.