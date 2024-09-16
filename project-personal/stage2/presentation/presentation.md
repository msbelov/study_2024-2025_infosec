---
## Front matter
lang: ru-RU
title: Лабораторная работа №1
subtitle: Установка и конфигурация операционной системы на виртуальную машину
author:
  - Белов М. С.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 01 января 1970

## i18n babel
babel-lang: russian
babel-otherlangs: english
mainfont: Arial
monofont: Courier New
fontsize: 12pt

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Задача

Установить операционную систему Rocky Linux. А также получить следующую информацию:
1. Версия ядра Linux (Linux version).
2. Частота процессора (Detected Mhz processor).
3. Модель процессора (CPU0).
4. Объем доступной оперативной памяти (Memory available).
5. Тип обнаруженного гипервизора (Hypervisor detected).
6. Тип файловой системы корневого раздела.



# Выполнение лабораторной работы

## Установка Rocky Linux

1. Создадим новую виртуальную машину. Укажем имя виртуальной машины **msbelov**, тип операционной системы — Linux, RedHat. Укажем размер основной памяти виртуальной машины — 2048 МБ. Зададим размер диска — 40 ГБ. После этого запустим виртуальную машину и скорректируем параметры установки.

## Установка Rocky Linux
![](image/1.png)

## Установка Rocky Linux

2. После успешной установки, подключим образ диска дополнений гостевой ОС:

![](image/2.png)

## Домашнее задание

Получим следующую информацию:
- Версия ядра Linux (Linux version).
- Частота процессора (Detected Mhz processor).
- Модель процессора (CPU0).

## Домашнее задание

![](image/3.png)
      
## Домашнее задание

- Объем доступной оперативной памяти (Memory available).
- Тип обнаруженного гипервизора (Hypervisor detected).
- Тип файловой системы корневого раздела.
- Последовательность монтирования файловых систем.

## Домашнее задание

![](image/4.png)

# Вывод

В ходе работы я приобрел практические навыки установки операционной системы на виртуальную машину.


