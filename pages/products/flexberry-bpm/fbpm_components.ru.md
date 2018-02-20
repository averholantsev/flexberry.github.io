---
title: Flexberry BPM
keywords: ember
sidebar: flexberry-bpm_sidebar
toc: false
permalink: ru/fbpm_components.html
lang: ru
---

## Семейство решений на основе jBPM  

Данный класс решений основывается на общей технологической базе – Jboss – семейство легких, облачных продуктов корпоративного уровня компании RedHat.  
Базовый продукт jBoss workflow version 1.0 был создан в 2003 году *(см. рисунок ниже)*. В 2011 году один из разработчиков jBPM Tom Baeyens перешёл в компанию Alfresco и используя спецификации и кодовую базу jBPM совместно с компанией Camunda создал BPMS Activiti.
В период 2003-2013 года на основе jBPM версии 3 подразделение консалтинговой группы РУНА создает BPMS runaWFE с поддержкой интеграции с Alfrecso.  
Версии jBoss workflow и решения на их основе представлены на рисунке:  
![](/images/pages/products/flexberry-bpm/family-bpms-products.png)

### jBPM  
Помимо основного ядра, обеспечивающего поддержку бизнес-процессов на протяжении всего жизненного цикла jBPM поддерживает множество дополнительных функций и инструментов:  
* Редактор Eclipse и веб-редактор для поддержки механизма графического создания бизнес-процессов (drag & drop).
* Поддержка подключаемых «ручных» задач и служб на основе WS-HumanTask для включения задач, выполняемых сотрудниками.
* Консоль управления, поддерживающая управление экземплярами процесса, списки задач и управление формой задачи, формирование отчетности.
* Дополнительный git-репозиторий моделей процессов для версионирования моделей и запуска необходимой версии процесса.
* Запись истории (для запросов / мониторинга / анализа).
* Интеграция с Seam, Spring, OSGi и т.д..  

Начиная с версии 6.0 совместно с jBPM в рамках компании RedHat стали развиваться и другие интеграционные продукты:  
* **Drools Rule Engine** – система управления бизнес-процессами на основе процессора правил.
* **KIE** *(Knowledge Is Everything)* – интеграционная система, включающая в себя кроме jBPM и Drools продукты:
  * **OptaPlanner** – система, обеспечивающая оптимизацию вариантов использования бизнес-ресурсов, таких как маршрутизация транспортных средств, составление расписаний, оптимизация облачных ресурсов, планирование заданий, оптимальной упаковки и т.п.
  * **UberFire** – веб-фреймворк для создания расширяемых рабочих столов и консольных приложений.
  * **Dashbuilder** – полнофункциональное веб-приложение, которое позволяет неспециалистам визуально создавать информационные интерфейсы (dashboard) для отображения и мониторинга бизнес-информации.  

Применение данных решений значительно расширяет гибкость создаваемых бизнес-решений и упрощает механизм создания конечного продукта.  

**Достоинства jBPM**  
* Высокая гибкость и простота динамической модификации создаваемых решений.
* Встроенная поддержка версионности моделей бизнес-процессов.
* Богатый набор инструментария по созданию качественного продукта с поддержкой аналитики и мониторинга бизнес-процессов.
* Широкие возможности по интеграции с внешними системами и приложениями. 
* Возможность моделирования сложных процессов.
* Поддержка docker-контейнеризации.  

**Недостатки jBPM**
* Высокие требования к аппаратному обеспечению сервера.  

### Activiti  
Функциональные возможности Activiti в целом совпадают с функциональными возможностями jBPM, так как оба проекта в процессе своего развития обменивались идеями.  
В рамках Activiti существует проект Camunda, в котором была реализована концепция механизма совместного использования процессов и встроенного механизма их обработки. Однако в настоящее время эти функциональные возможности также внедрены и в Activiti.  
В настоящее время оба проекта разделяют общую кодовую базу. Activiti более ориентирована на разработчиков ПО, Camunda – на потребителей.  

**Достоинства Activiti**
* Широкие возможности по интеграции с внешними системами и приложениями.
* Поддержка механизма совместного использования процессов и встроенного механизма их обработки.
* Возможность моделирования сложных процессов.
* Поддержка системы управления документооборотом Alfresco.  

**Недостатки Activiti**  
* Тяжеловесность создаваемых решений.
* Ограниченный список поддерживаемых баз данных.  

### RunaWFE
**RunaWFE** – свободная система управления бизнес-процессами и административными регламентами с открытым кодом. Распространяется под свободной лицензией LGPL. RunaWFE использует как собственные решения, так и некоторые идеи проектов JBoss jBPM и Activiti, содержит большое количество компонентов, задача которых – обеспечить удобную работу конечного пользователя.  

**Достоинства RunaWFE**  
* Возможность интеграции существующих разнородных приложений предприятия.
* Простая интеграция с реляционными базами данных.
* Боты для выполнения автоматических заданий.
* Система безопасности, позволяющая интеграцию с LDAP/MS Active Directory.
* Интеграция с Alfresco.
* Локализация на русский язык.  

**Недостатки RunaWFE**
* Ориентация на довольно старую кодовую базу jBPM.  
