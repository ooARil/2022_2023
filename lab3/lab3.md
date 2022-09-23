---
# Front matter
lang: ru-Ru
title: "Лабораторная работа №3"
subtitle: "Дискреционное разграничение прав в Linux. Два пользователя"
author: "Ильинский Арсений Александрович"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: xelatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

# Задание

Выполнить задания из лабораторной работы и проанализировать полученные результаты.

# Теоретическое введение

Для выполнения данной лабораторной нет специальной теории. 

# Выполнение лабораторной работы

Последовательно выполнил все пункты, занося ответы на поставленные вопросы и замечания в отчет:

1. В прошлой лабораторной работе был создан пользователь guest с помощью команды useradd guest:
   
   ![Создание пользователя guest2](images/1.png){#fig:001}
   
2. В прошлой лабораторной работе был задан пароль пользователю guest с помощью команды passwd guest:
   
   ![Задание пароля пользователя guest](images/2.png){#fig:002}
   
   ![Пользователь guest](images/3.png){#fig:003}


3. Провел аналогичную процедуры создания еще одного пользователя guest2:

   ![Создание пользователя guest2](images/4.png){#fig:004}

4. Добавил пользователя guest2 в группу guest:

   ![Добавление пользователя guest2 в группу guest](images/5.png){#fig:005}

5. Осуществил вход в систему от двух пользователей на двух разных консолях: guest на первой консоли:

   ![Вход в систему от пользователя guest](images/6.png){#fig:006}

    и guest2 на второй консоли:

   ![Вход в систему от пользователя guest2](images/7.png){#fig:007}

6. Для обоих пользователей командой *pwd* определил директорию, в которой они находятся. Вывод совпадает с приглашением командной строки. Оба пользователя находятся в домашней директории пользователя guest:

   ![Нахождение пользователя guest](images/8.png){#fig:008}

   ![Нахождение пользователя guest2](images/9.png){#fig:009}

7. Уточнил имя пользователя: 

   ![Имя пользователя guest](images/10.png){#fig:010}

   ![Имя пользователя guest2](images/11.png){#fig:011}

   его группу, кто входит в неё и к каким группам принадлежит он сам:

   ![Группа пользователя guest, кто входит в неё и к каким группам принадлежит он сам](images/12.png){#fig:012}

   ![Группа пользователя guest2, кто входит в неё и к каким группам принадлежит он сам](images/13.png){#fig:013}

   Определил командами *groups guest* и *groups guest2*, в какие группы входят пользователи guest и guest2:

   ![Группы пользователей guest и guest2 : терминал guest](images/14.png){#fig:014}

   ![Группы пользователей guest и guest2 : терминал guest2](images/15.png){#fig:015}

   Первая команда выводит на экран группы пользователя, но без уточнения к какому пользователю относятся группы, т.к. команды работаю только для пользователя, через которого открыта консоль. Вторая команда выводи код группы пользователя:

   ![Группы пользователя guest](images/16.png){#fig:016}

   ![Группы пользователя guest2](images/17.png){#fig:017}

8. Сравнил полученную информацию с содержимым файла */etc/group*:

   ![Вывод команды cat /etc/group для guest (1/2)](images/18.png){#fig:018}

   ![Вывод команды cat /etc/group для guest (2/2)](images/19.png){#fig:019}

   ![Вывод команды cat /etc/group для guest2 (1/2)](images/20.png){#fig:020}

   ![Вывод команды cat /etc/group для guest2 (2/2)](images/21.png){#fig:021}

   Вывод команды совпадает с данными, полученными на предыдущих шагах.

9. От имени пользователя guest2 выполнил регистрацию пользователя guest2 в группе guest:

   ![Регистрация пользователя guest2 в группе guest](images/22.png){#fig:022}

10. От имени пользователя guest изменил права директории */home/guest*, разрешив все действия для пользователей группы, а затем снял все атрибуты доступа с директории */home/guest/dir1*:

    ![Изменение прав на директории пользователя guest](images/23.png){#fig:023}

    Меняя атрибуты у директории *dir1* и файла *file1* от имени пользователя guest и делая проверку от пользователя guest2, заполнил таблицу ниже, определяя опытным путём, какие операции разрешены, а какие нет:

    ![Таблица 3.1 (1/6)](images/24.png){#fig:024}

    ![Таблица 3.1 (2/6)](images/25.png){#fig:025}

    ![Таблица 3.1 (3/6)](images/26.png){#fig:026}

    ![Таблица 3.1 (4/6)](images/27.png){#fig:027}

    ![Таблица 3.1 (5/6)](images/28.png){#fig:028}

    ![Таблица 3.1 (6/6)](images/29.png){#fig:029}

    Полученная таблица не совпадает с таблицей из прошлой лабораторной работы, поскольку члены группы не имеют права изменять атрибуты файла. Для остальных операций члену группы нужны такие же права, как у владельца.

    На основании заполненной таблицы 3.1 определил те или иные минимально необходимые права для выполнения пользователем guest2 операций внутри директории dir1 и заполню таблицу:

    ![Таблица 3.2 : минимальн необходимые права для выполнения операций](images/30.png){#fig:030}

# Выводы

Благодаря данной лабораторной работы я приобрел практические навыки работы в консоли с атрибутами файлов для групп пользователей, а также на практике закрепил теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux (дистрибутив - Rocky).


# Список литературы

- <code>[Кулябов Д.С., Королькова А.В., Геворкян М.Н *Лабораторная работа №3*](https://esystem.rudn.ru/pluginfile.php/1651749/mod_resource/content/4/003-lab_discret_2users.pdf)</code>