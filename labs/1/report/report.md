---
## Front matter
title: "Отчёт по лабораторной работе №1"
subtitle: "Установка и конфигурация операционной системы на виртуальную машину"
author: "Морозов Михаил Евгеньевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---


# Цель работы

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Техническое обеспечение

Я буду использовать Parallels тк, у меня ARM процессор и я не могу поставить VirtualBox[@VM:bash].

# Выполнение лабораторной работы

Скачали iso-файл диструбутива с официального сайта для архитектуры arm и создали новую систему с параметрами из видео а туис (рис. [-@fig:001])

![Параметры системы](image/0.png){#fig:001 width=70%}

Запустили нашу систему и начали установку Centos следуя этапам из видео, и запустили систему (рис. [-@fig:002])

![Система](image/1.png){#fig:002 width=70%}


Получим следующую информацию, используя команду dmesg | grep для поиска:

1. Версия ядра Linux (Linux version) - (рис. [-@fig:006])
2. Частота процессора (Detected Mhz processor) - (рис. [-@fig:006])
3. Модель процессора (CPU0) - (рис. [-@fig:006])
4. Объем доступной оперативной памяти (Memory available) - (рис. [-@fig:006])
5. Тип обнаруженного гипервизора (Hypervisor detected) - (рис. [-@fig:006])

![Пункты 1-5](image/2.png){#fig:006 width=70%}

6. Тип файловой системы корневого раздела - (рис. [-@fig:007])
7. Последовательность монтирования файловых систем. - (рис. [-@fig:007])

![Пункты 6-7](image/3.png){#fig:009 width=70%}

# Ответы на контрольные вопросы

1. Какую информацию содержит учётная запись пользователя? - *Системное имя, id пользователя, id группы, полное имя, домашний каталог, оболочка и пароль*
2. Укажите команды терминала и приведите примеры:
– для получения справки по команде - *help*
– для перемещения по файловой системе - *cd*
– для просмотра содержимого каталога - *ls*
– для определения объёма каталога - *du*
– для создания / удаления каталогов / файлов - *mkdir/ rm -r для директорий, touch/rm для файлов* 
– для задания определённых прав на файл / каталог - *chmod*
– для просмотра истории команд - *history*
3. Что такое файловая система? - *архитектура хранения данных в операционной системе*
Приведите примеры с краткой характеристикой - *ExFAT - файловая система предназначенная для Flash-накопителей, ext4 - современная файловая система, стандартная для Linux*
4. Как посмотреть, какие файловые системы подмонтированы в ОС? - *findmnt*
5. Как удалить зависший процесс? - *kill*

# Выводы

Установили Centos на виртуальную машину и получили практические навыки по установке и настройке операционных систем на виртуальных машинах. 

# Список литературы{.unnumbered}

::: {#refs}
:::
