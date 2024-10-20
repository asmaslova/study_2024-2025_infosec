---
## Front matter
lang: ru-RU
title: Лабораторная работа №3
subtitle: "Дискреционное разграничение прав в Linux. Два пользователя"
author:
  - Маслова А. С.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 20 сентября 2024

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

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Маслова Анастасия Сергеевна
  * студентка группы НКНбд-01-21
  * Российский университет дружбы народов
  * [1032216455@rudn.ru](mailto:1032216455@rudn.ru)
  * <https://github.com/asmaslova/>

:::
::: {.column width="30%"}

![](./image/me.JPG)

:::
::::::::::::::

# Цель работы

## Цель работы

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

# Выполнение лабораторной работы

## Выполнение лабораторной работы

![Создание пользователей guest и guest1](image/18.png){#fig:001 width=70%}

## Выполнение лабораторной работы

![Выполнение пунктов 6 и 7 для пользователя guest](image/1.png){#fig:002 width=70%}

## Выполнение лабораторной работы

![Выполнение пунктов 6 и 7 для пользователя guest1](image/19.png){#fig:003 width=70%}

## Выполнение лабораторной работы

![Содержимое файла /etc/group у пользователя guest, часть 1](image/2.png){#fig:004 width=70%}

## Выполнение лабораторной работы

![Содержимое файла /etc/group у пользователя guest, часть 2](image/3.png){#fig:005 width=70%}

## Выполнение лабораторной работы

![Содержимое файла /etc/group у пользователя guest1, часть 1](image/4.png){#fig:006 width=70%}

## Выполнение лабораторной работы

![Содержимое файла /etc/group у пользователя guest1, часть 2](image/5.png){#fig:007 width=70%}

## Выполнение лабораторной работы

![Регистрация пользователя guest2 в группе guest командой newgrp guest](image/20.png){#fig:008 width=70%}

## Выполнение лабораторной работы

![Изменение права директории /home/guest от имени пользователя guest](image/21.png){#fig:009 width=70%}

## Выполнение лабораторной работы

: Минимальные права для совершения действий {#tbl:3-2}

|        Операция        | Минимальные права на директорию | Минимальные права на файл |
|------------------------|---------------------------------|---------------------------|
| Создание файла | 030 | 030 |
| Удаление файла | 030 | 030 |
| Чтение файла | 010 | 010 |
| Запись в файл | 010 | 010 |
| Переименование файла | 030 | 030 |
| Создание поддиректории | 030 | 030 |
| Удаление поддиректории | 030 | 030 |

# Вывод

## Вывод

В ходе лабораторной работы я получила практические навыки работы в консоли с атрибутами файлов для групп пользователей. 