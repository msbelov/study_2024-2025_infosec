---
## Front matter
title: "Лабораторная работа №1"
subtitle: "Установка и конфигурация операционной системы на виртуальную машину"
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.


# Задание

Установить операционную систему Rocky Linux. А также получить следующую информацию:
1. Версия ядра Linux (Linux version).
2. Частота процессора (Detected Mhz processor).
3. Модель процессора (CPU0).
4. Объем доступной оперативной памяти (Memory available).
5. Тип обнаруженного гипервизора (Hypervisor detected).
6. Тип файловой системы корневого раздела.

# Выполнение лабораторной работы

### Установка Rocky Linux

1. Создадим новую виртуальную машину. Укажем имя виртуальной машины **msbelov**, тип операционной системы — Linux, RedHat. Укажем размер основной памяти виртуальной машины — 2048 МБ. Зададим размер диска — 40 ГБ. После этого запустим виртуальную машину и скорректируем параметры установки.

![Установка Rocky](image/1.png){ #fig:001 width=70% }


2. После успешной установки, подключим образ диска дополнений гостевой ОС:

![Подключение образа диска дополнений гостевой ОС](image/2.png){ #fig:002 width=70% }


### Домашнее задание 
Получим следующую информацию:
- Версия ядра Linux (Linux version).
- Частота процессора (Detected Mhz processor).
- Модель процессора (CPU0).

![Версия ядра, частота процессора, модель процессора](image/3.png){ #fig:003 width=70% }

- Объем доступной оперативной памяти (Memory available).
- Тип обнаруженного гипервизора (Hypervisor detected).
- Тип файловой системы корневого раздела.
- Последовательность монтирования файловых систем.

![Память, гипервизор, FS, последовательность монтирования файловых систем](image/4.png){ #fig:004 width=70% }


# Вывод

В ходе работы я приобрел практические навыки установки операционной системы на виртуальную машину.

# Контрольные вопросы

**1. Какую информацию содержит учётная запись пользователя?**

- Учётная запись пользователя содержит: уникальное имя пользователя (username), уникальный идентификатор пользователя (UID), идентификатор группы (GID), домашний каталог, интерпретатор команд (shell), а также пароль.

**2. Укажите команды терминала и приведите примеры:**

- **для получения справки по команде:** `man <команда>` (например: `man ls`)
- **для перемещения по файловой системе:** `cd <путь>` (например: `cd /home/user`)
- **для просмотра содержимого каталога:** `ls <путь>` (например: `ls /home`)
- **для определения объёма каталога:** `du -sh <каталог>` (например: `du -sh /var/log`)
- **для создания / удаления каталогов / файлов:**  
  - Создание каталога с помощью `mkdir <каталог>` (например: `mkdir /home/user/newdir`)
  - Удаление каталога с помощью `rmdir <каталог>` (например: `rmdir /home/user/newdir`)
  - Создание файла с помощью `touch <файл>` (например: `touch /home/user/newfile.txt`)
  - Удаление файла с помощью `rm <файл>` (например: `rm /home/user/newfile.txt`)
- **для задания определённых прав на файл / каталог:** `chmod <права> <файл/каталог>` (например: `chmod 755 /home/user/script.sh`)
- **для просмотра истории команд:** `history`

**3. Что такое файловая система? Приведите примеры с краткой характеристикой.**

- Файловая система — это способ организации, хранения и управления данными на носителях. Примеры:
  - **ext4:** стандартная файловая система для большинства дистрибутивов Linux, поддерживает большие файлы и разделы.
  - **NTFS:** файловая система, используемая в Windows, поддерживает сжатие данных и восстановление после сбоев.
  - **FAT32:** простая и широко поддерживаемая файловая система, но имеет ограничения на размер файлов и разделов.

**4. Как посмотреть, какие файловые системы подмонтированы в ОС?**

- Для просмотра подмонтированных файловых систем можно использовать команды `mount` или `df -h`.

**5. Как удалить зависший процесс?**

- Для удаления зависшего процесса следует воспользоваться командой `kill <PID>`, где `PID` — идентификатор процесса (например: `kill 1234`). Если процесс не завершился, можно использовать `kill -9 <PID>`.
