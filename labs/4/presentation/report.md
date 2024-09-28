---
## Front matter
title: "Отчёт по лабораторной работе №4"
subtitle: "Дискреционное разграничение прав в Linux. Расширенные атрибуты"
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

Получение практических навыков работы в консоли с расширенными атрибутами файлов.

# Теоретическое введение

chattr — команда, изменяющая атрибуты файлов на файловых системах ext2fs, ext3, ext4 и частично на других файловых системах Linux.
Операторы 
- "+" обозначает добавление указанных атрибутов к существующим
- "-" обозначает их снятие
- "=" обозначает установку только этих атрибутов файлам.

Символы "ASacDdijsu" указывают на новые атрибуты файлов.

# Выполнение лабораторной работы

Попробуем добавить атрибут к файлу от имени записи guest.
Получаем ошибку, поэтому делаем это от имени администратора
Посмотрим сработала ли команда
К файлу добавился атбрибут "a"
Попробуем различные действия с этим файлом.
Сработала только команда чтения
Пробуем дальше
Несмотря на то, что владелец файла может читать и редактировать его по модификаторам доступа, мы не можем менять его как хотим
Пробуем дальше
Сработала только команда дозаписи в файл, то есть файл открыт только для добавления информации в него
Теперь снимем атрибут "a" и поставим "i"
Меняем атрибуты
Так же попробуем выполнить разные дейтсвия с файлом, чтобы понять для чего нужен этот атрибут.
Ни одна команда, меняющая файл не проходит, значит атрибут i указывает на то, что файл неизменяемый

Результаты работы команд
1 (рис. [-@fig:001])
![1](image/1.PNG){#fig:007 width=70%}

2 (рис. [-@fig:002])
![2](image/2.PNG){#fig:002 width=70%}

3 (рис. [-@fig:003])
![3](image/3.PNG){#fig:003 width=70%}

# Выводы

Получили практических навыков работы в консоли с расширенными атрибутами файлов.