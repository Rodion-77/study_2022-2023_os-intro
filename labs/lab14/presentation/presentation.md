---
## Front matter
lang: ru-RU
title: Лабораторная работа № 14 
subtitle: Программирование в командном процессоре ОС UNIX. Расширенное программирование
author:
  - Павличенко Родион Андреевич
institute:
  - Российский университет дружбы народов, Москва, Россия

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
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Павличенко Родион Андреевич
  * студент
  * Российский университет дружбы народов
  * [1132246838@pfur.ru](mailto:1132246838@pfur.ru)
  
:::
::: {.column width="30%"}

:::
::::::::::::::

# Выполнение лабораторной работы

## Написали командный файл, реализующий упрощённый механизм семафоров.

:::::::::::::: {.columns align=center}
::: {.column width="30%"}

![](image/1.png)

:::
::::::::::::::

## Реализовали команду man с помощью командного файла. 

:::::::::::::: {.columns align=center}
::: {.column width="30%"}

![](image/2.png)

:::
::::::::::::::


## Используя встроенную переменную $RANDOM, написали командный файл, генерирующий случайную последовательность букв латинского алфавита. Учли, что $RANDOM выдаёт псевдослучайные числа в диапазоне от 0 до 32767

:::::::::::::: {.columns align=center}
::: {.column width="30%"}

![](image/3.png)

:::
::::::::::::::



## Вывод

Изучили основы программирования в оболочке ОС UNIX. Научились писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.

