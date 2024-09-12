---
## Front matter
title: "Индивидуальный проект"
subtitle: "Этап 1. Установка Kali Linux"
author: "Белов Максим Сергеевич, НПИбд-01-21"

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
mainfont: Times New Roman
romanfont: PT Serif
sansfont: DejaVu Sans
monofont: DejaVu Sans Mono
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

Целью данной работы является установка Kali Linux в VirtualBox.


# Задание

Установить дистрибутив Kali Linux в виртуальную машину.

# Выполнение лабораторной работы

## Установка Kali Linux

1. Создадим новую виртуальную машину. Укажем имя виртуальной машины **msbelov_kali**. Укажем размер основной памяти виртуальной машины — 2048 МБ. Зададим размер диска — 40 ГБ. После этого запустим виртуальную машину и скорректируем параметры установки.

![Установка Kali](image/1.png){ #fig:001 width=100% }


2. Выберем наше местоположение

![Местоположение](image/2.png){ #fig:002 width=100% }

3. Напишем имя хоста - **msbelov.localdomain**

![Имя хоста](image/3.png){ #fig:003 width=100% }

4. Напишем имя пользователя - **msbelov**

![Имя пользователя](image/4.png){ #fig:004 width=100% }

5. После успешной установки, авторизуемся в систему.

![Заход в систему](image/5.png){ #fig:005 width=100% }


![Kali Linux](image/6.png){ #fig:006 width=100% }


# Вывод

В ходе работы я установил Kali Linux в VirtualBox.
