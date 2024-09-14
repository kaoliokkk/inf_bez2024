---
## Front matter
title: "1 Этап Индвидуального проекта"
subtitle: "Установка  Kali Linux"
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

Целью данной работы является установка Kali Linux на свой компьютер.

# Техническое обеспечение

Я буду использовать Parallels тк, у меня ARM процессор и я не могу поставить VirtualBox[@VM:bash].

# Выполнение лабораторной работы

Скачали iso-файл диструбутива с официального сайта для архитектуры arm и создали новую систему. (рис. [-@fig:001])

![Сайт](image/1.png){#fig:001 width=70%}

Запустили нашу систему и начали установку Kali Linux следуя этапам из видео, и запустили систему (рис. [-@fig:002])

![Система](image/2.png){#fig:002 width=70%}

Проверили что теперь нам доступны и Centos и Kali Linux. (рис. [-@fig:003])

![2 Системы](image/3.png){#fig:003 width=70%}


# Выводы

Установили Kali Limux на виртуальную машину и получили практические навыки по установке и настройке операционных систем на виртуальных машинах. 

# Список литературы{.unnumbered}

::: {#refs}
:::
