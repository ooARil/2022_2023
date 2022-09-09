---
# Front matter
lang: ru-Ru
title: "Лабораторная работа №1"
subtitle: "Установка дистрибутива Rocky"
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

Приобретение практических навыков установки операционной системы Rocky на виртуальную машину, а также настройка минимально необходимого окружения для дальнейшей работы.

# Задание

Установить и настроить дистрибутив Rocky на виртуальную машину, а также установить дополнения необходимые для дальнейшей работы.

# Теоретическое введение

Для выполнения данной лабораторной нет специальной теории. 

# Выполнение лабораторной работы

**Первым шагом** необходимо скачать DVD-образ операционной системы (дистрибутив Rocky) под архитектуру нашего компьютера:

![Скачивание DVD-образа операционной системы (дистрибутив Rocky)](images/1.png){#fig:001}

**Вторым шагом** необходимо определить каталог, в который будут храниться машины:

![Создание папки, в которой хранятся машины](images/2.png){#fig:002}

**Третьим шагом** необходимо создать виртуальную машины в VirtualBox. Для этого выбираем ***Машина -> Создать***:

1. Сначала указываем имя и тип ОС:

   ![Создание виртуальной машины](images/3.png){#fig:003}

2. Затем указываем объем оперативной памяти, выделенный виртуальной машине:

   ![Объем оперативной памяти](images/4.png){#fig:004}

3. Далее создаем новый динамический виртуальный жесткий диск типа VDI и задаем его размер:

   ![Создание виртуального жесткого диска](images/5.png){#fig:005}

   ![Тип виртуального жесткого диска](images/6.png){#fig:006}

   ![Формат хранения](images/7.png){#fig:007}

   ![Размер виртуального жесткого диска](images/8.png){#fig:008}

**Четвертым шагом** в VirtualBox заходим в ***Настройки -> Носители*** и добавляем новый привод оптических дисков, где выбираем заранее скачанный образ выбранной операционной системы.

![Выбор образа операционной системы](images/9.png){#fig:009}

**Пятым шагом** запускаем виртуальную машину и начинаем установку ОС.

![Старт установки ОС](images/10.png){#fig:010}

По ходу начальной настройки ОС перед ее установкой нужно выполнить несколько шагов.

1. Выбрать язык:

   ![Выбор языка](images/11.png){#fig:011}

2. Настроить часовой пояс:

   ![Выбор часового пояса](images/12.png){#fig:012}

3. Скорректировать раскладку клавиатуры:

   ![Раскладка клавиатуры](images/13.png){#fig:013}

4. Выбрать пакет предустановленных программ:

   ![Выбор пакета программ](images/14.png){#fig:014}

5. Отключить KDUMP:

   ![Отключение KDUMP](images/15.png){#fig:015}

6. Место установки ОС оставить без изменения:

   ![Место установки ОС](images/16.png){#fig:016}

7. Включить сетевое соединение, с именем узла arilinskiy.localadmin:

   ![Включение сетевого соединения](images/17.png){#fig:017}

8. Установить пароль для root:

   ![Задание пароля для root](images/18.png){#fig:018}

9. Создать пользователя с правами администратора:

   ![Создание пользователя](images/19.png){#fig:019}

10. Правильно перезагрузить систему:

    ![Перезагрузка системы (1/2)](images/20.png){#fig:020}

    ![Перезагрузка системы (2/2)](images/21.png){#fig:021}

После выполнения данных шагов мы попадаем на рабочий стол нашей виртуальной машины. Для более удобной работы с машиной нужно подключить образ диска дополнительной гостевой ОС. Чтобы это сделать, необходимо в меню ***Устройства*** окна VirtualBox выбрать опцию подключения диска дополнительной гостевой ОС. После чего появится всплывающее окно, в котором можно запустить данный процесс:

![Запуск подключения диска дополнительной гостевой ОС (1/2)](images/22.png){#fig:022}

![Запуск подключения диска дополнительной гостевой ОС (2/2)](images/23.png){#fig:023}

На этом установка дистрибутива Rocky на виртуальную машину завершается.

## Домашнее задание

С помощью утилит *dmesg* и *grep* требуется найти некоторую информацию о системе:

1. Версия ядра Linux: 5.14.0-0.70.13.1
2. Частота процессора: 2195.874 MHz
3. Модель процессора: AMD Ryzen 7 2700U with Radeon Vega Mobile Gfx
4. Объем доступной памяти: 240380k
5. Тип обнаруженного гипервизора: KVM
6. Тип файловой системы корневого раздела: XFS

![Информация о системе](images/24.png){#fig:024}

# Выводы

Благодаря данной лабораторной работе я приобрел практические навыки установки операционной системы Rocky на виртуальную машину, а также получил знания по настройке минимально необходимого окружения для дальнейшей работы.


# Список литературы

- <code>[Кулябов Д.С., Королькова А.В., Геворкян М.Н *Лабораторная работа №1*](https://esystem.rudn.ru/mod/folder/view.php?id=892013)</code>