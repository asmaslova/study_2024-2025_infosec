---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Дискреционное разграничение прав в Linux. Расширенные атрибуты"
author: "Маслова Анастасия Сергеевна"

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

# Выполнение лабораторной работы

1. От имени пользователя guest определите расширенные атрибуты файла /home/guest/dir1/file1 командой `lsattr /home/guest/dir1/file1`
2. Установите командой `chmod 600 file1` на файл file1 права, разрешающие чтение и запись для владельца файла (рис. [@fig:001]).

![Выполнение пунктов 1-6](image/1.png){#fig:001 width=70%}

3. Попробуйте установить на файл /home/guest/dir1/file1 расширенный атрибут a от имени пользователя guest: `chattr +a /home/guest/dir1/file1`

При попытке установить расширенный атрибут а от имени пользователя появлется запрет (рис [@fig:001]).

4. Зайдите на третью консоль с правами администратора либо повысьте свои права с помощью команды su. Попробуйте установить расширенный атрибут a на файл /home/guest/dir1/file1 от имени суперпользователя: `chattr +a /home/guest/dir1/file1`

Повысив свои права с помощью команды su, я смогла установить расширенный атрибут а на файл (рис. [@fig:001]).

5. От пользователя guest проверьте правильность установления атрибута: `lsattr /home/guest/dir1/file1`

6. Выполните дозапись в файл file1 слова «test» командой `echo "test" /home/guest/dir1/file1`. После этого выполните чтение файла file1 командой `cat /home/guest/dir1/file1`. Убедитесь, что слово test было успешно записано в file1.

К сожалению, слово не было успешно записано в файл (рис. [@fig:001]).

7. Попробуйте удалить файл file1 либо стереть имеющуюся в нём информацию командой `echo "abcd" > /home/guest/dirl/file1`. Попробуйте переименовать файл.

Ничего из этого у меня не получилось.

8. Попробуйте с помощью команды `chmod 000 file1` установить на файл file1 права, например, запрещающие чтение и запись для владельца файла. Удалось ли вам успешно выполнить указанные команды?

Установив на файл права 000, я не смогла сделать с ним вообще ничего, даже удалить впоследствии. Даже с правами суперпользователя. В связи с этим мне пришлось выполнять дальнейшие пункты с новым файлом file01 (не путать с изначальным file1).

9. Снимите расширенный атрибут a с файла /home/guest/dirl/file1 от имени суперпользователя командой `chattr -a /home/guest/dir1/file1`. Повторите операции, которые вам ранее не удавалось выполнить. Ваши наблюдения занесите в отчёт.

Поставив на новый файл file01 права 600 и не добавляя в этот раз атрибут, я попробовала проделать все те же действия с этим файлом, и у меня все получилось.

10. Повторите ваши действия по шагам, заменив атрибут «a» атрибутом «i». Удалось ли вам дозаписать информацию в файл? Ваши наблюдения занесите в отчёт.

Заменив атрибут а на атрибут i, я проделала все те же действия и получила результат.

# Выводы

В результате выполнения работы я повысила свои навыки использования интерфейса командой строки (CLI), познакомилась на примерах с тем, как используются основные и расширенные атрибуты при разграничении доступа. Также я имела возможность связать теорию дискреционного разделения доступа (дискреционная политика безопасности) с её реализацией на практике в ОС Linux и составила наглядные таблицы, поясняющие, какие операции возможны при тех или иных установленных правах, после чего опробовала действие на практике расширенных атрибутов «а» и «i».

# Список литературы{.unnumbered}

::: {#refs}
:::