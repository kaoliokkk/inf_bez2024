---
## Front matter
lang: ru-RU
title: "1 Этап Индвидуального проекта"
subtitle: "Установка  Kali Linux"
author:
  - Морозов М. Е.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 13 сентября 2024

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


## Цель работы

Целью данной работы является установка Kali Linux на свой компьютер.

## Техническое обеспечение

Я буду использовать Parallels тк, у меня ARM процессор и я не могу поставить VirtualBox.

## Выполнение первого этапа

Скачали iso-файл диструбутива с официального сайта для архитектуры arm и создали новую систему. (рис. [-@fig:001])

## Выполнение первого этапа

![Сайт](image/1.png){#fig:001 width=70%}

## Выполнение первого этапа

Запустили нашу систему и начали установку Kali Linux следуя этапам из видео, и запустили систему. (рис. [-@fig:002])

## Выполнение первого этапа

![Система](image/2.png){#fig:002 width=70%}

## Выполнение первого этапа


Проверили что теперь нам доступны и Centos и Kali Linux. (рис. [-@fig:003])

## Выполнение первого этапа

![2 Системы](image/3.png){#fig:003 width=70%}


# Выводы

Установили Kali Linux на виртуальную машину и получили практические навыки по установке и настройке операционных систем на виртуальных машинах. 

## Список литературы

1. VirtualBox [Электронный ресурс]. Oracler, 2024. URL: https://www.virtualbox.org/.

