---
## Front matter
lang: ru-RU
title: Лабораторная работа № 1
subtitle: Установка и конфигурация операционной системы на виртуальную машину
author:
  - Морозов М. Е.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 6 сентября 2024

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Информация

## Цель работы

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

## Техническое обеспечение

Я буду использовать Parallels тк, у меня ARM процессор и я не могу поставить VirtualBox[@VM:bash].

# Выполнение лабораторной работы

## Скачали iso-файл диструбутива с официального сайта для архитектуры arm и создали новую систему с параметрами из видео а туис (рис. [-@fig:001])

![Параметры системы](image/0.png){#fig:001 width=70%}

## Запустили нашу систему и начали установку Centos следуя этапам из видео, и запустили систему (рис. [-@fig:002])

![Система](image/1.png){#fig:002 width=70%}


## Получим следующую информацию, используя команду dmesg | grep для поиска:

1. Версия ядра Linux (Linux version) - (рис. [-@fig:006])
2. Частота процессора (Detected Mhz processor) - (рис. [-@fig:006])
3. Модель процессора (CPU0) - (рис. [-@fig:006])
4. Объем доступной оперативной памяти (Memory available) - (рис. [-@fig:006])
5. Тип обнаруженного гипервизора (Hypervisor detected) - (рис. [-@fig:006])

## ![Пункты 1-5](image/2.png){#fig:006 width=70%}

## Получим следующую информацию, используя команду dmesg | grep для поиска:

6. Тип файловой системы корневого раздела - (рис. [-@fig:007])
7. Последовательность монтирования файловых систем. - (рис. [-@fig:007])

## ![Пункты 6-7](image/3.png){#fig:009 width=70%}

# Ответы на контрольные вопросы

## 1. Какую информацию содержит учётная запись пользователя? - *Системное имя, id пользователя, id группы, полное имя, домашний каталог, оболочка и пароль*
## 2. Укажите команды терминала и приведите примеры:
– для получения справки по команде - *help*
– для перемещения по файловой системе - *cd*
– для просмотра содержимого каталога - *ls*
– для определения объёма каталога - *du*
– для создания / удаления каталогов / файлов - *mkdir/ rm -r для директорий, touch/rm для файлов* 
– для задания определённых прав на файл / каталог - *chmod*
– для просмотра истории команд - *history*
## 3. Что такое файловая система? - *архитектура хранения данных в операционной системе*
Приведите примеры с краткой характеристикой - *ExFAT - файловая система предназначенная для Flash-накопителей, ext4 - современная файловая система, стандартная для Linux*
## 4. Как посмотреть, какие файловые системы подмонтированы в ОС? - *findmnt*
## 5. Как удалить зависший процесс? - *kill*

## Выводы

Установили Centos на виртуальную машину и получили практические навыки по установке и настройке операционных систем на виртуальных машинах. 

## Список литературы

1. VirtualBox [Электронный ресурс]. Oracler, 2024. URL: https://www.virtualbox.org/.

