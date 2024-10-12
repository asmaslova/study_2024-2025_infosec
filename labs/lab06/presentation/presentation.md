---
## Front matter
lang: ru-RU
title: Лабораторная работа №6
subtitle: "Мандатное разграничение прав в Linux"
author:
  - Маслова А. С.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 12 октября 2024

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

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux1. Проверить работу SELinx на практике совместно с веб-сервером Apache.

# Выполнение лабораторной работы

## Выполнение лабораторной работы

![Выполнение команд `getenforce и sestatus`](image/1.png){#fig:001 width=70%}

## Выполнение лабораторной работы

![Выполнение команды `service httpd status`](image/2.png){#fig:002 width=70%}

## Выполнение лабораторной работы

![Выполнение `команды ps auxZ | grep httpd`](image/3.png){#fig:003 width=70%}

## Выполнение лабораторной работы

![Выполнение команды `sestatus -bigrep httpd`](image/4-1.png){#fig:004 width=70%}

## Выполнение лабораторной работы

![Выполнение команды `seinfo`](image/5.png){#fig:006 width=70%}

## Выполнение лабораторной работы

![Выполнение команды `ls -lZ /var/www`](image/6.png){#fig:007 width=70%}

## Выполнение лабораторной работы

![Выполнение команды `ls -lZ /var/www/html`](image/7.png){#fig:008 width=70%}

## Выполнение лабораторной работы

![Создание html-файл /var/www/html/test.html](image/9.png){#fig:009 width=70%}

## Выполнение лабораторной работы

![Проверка контекста созданного мною файла](image/10.png){#fig:010 width=70%}

## Выполнение лабораторной работы

![Обращение к файлу через веб-сервер](image/11.png){#fig:011 width=70%}

## Выполнение лабораторной работы

![Проверка контекста файла test.html](image/12.png){#fig:012 width=70%}

## Выполнение лабораторной работы

![Изменение контекста файла test.html](image/13.png){#fig:013 width=70%}

## Выполнение лабораторной работы

![Доступ к файлу через веб-сервер](image/14.png){#fig:014 width=70%}

## Выполнение лабораторной работы

![Просмотр системного лог-файла](image/15.png){#fig:015 width=70%}

## Выполнение лабораторной работы

![Перезапуск веб-сервера Apache](image/16-17.png){#fig:016 width=70%}

## Выполнение лабораторной работы

![Выполнение команды `tail -nl /var/log/messages`](image/18-1.png){#fig:017 width=70%}

## Выполнение лабораторной работы

![Выполнение команды `semanage port -a -t http_port_t -р tcp 81` и проверка списка портов](image/19.png){#fig:019 width=70%}

## Выполнение лабораторной работы

![Запуск веб-сервера Apache](image/20.png){#fig:020 width=70%}

## Выполнение лабораторной работы

![Возвращение контекста httpd_sys_cоntent__t к файлу /var/www/html/ test.html](image/21-1.png){#fig:021 width=70%}

## Выполнение лабораторной работы

![Получение доступа к файлу через веб-сервер](image/21-2.png){#fig:022 width=70%}

## Выполнение лабораторной работы

![Исправление конфигурационного файла apache](image/22.png){#fig:023 width=70%}

## Выполнение лабораторной работы

![Удаление привязки http_port_t к 81 порту](image/23.png){#fig:024 width=70%}

## Выполнение лабораторной работы

![Удаление файла /var/www/html/test.html](image/24.png){#fig:025 width=70%}

# Вывод

## Вывод

В ходе лабораторной работы я развила навыки администрирования ОС Linux, получила первое практическое знакомство с технологией SELinux1 и проверила работу SELinx на практике совместно с веб-сервером Apache.