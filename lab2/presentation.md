---
marp: true
paginate: true
author: Ilyinsky A. Arseniy
theme: default
---
<style>
section::after {
  content: attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
}
img[alt="center"] {
     display: block;
     margin: 0 auto;
}
th {
    font-size: 25px;
}
td {
    font-size: 25px;
}
img[alt="center"] {
    display: block;
    margin: 0 auto;
}
h1 {
    font-size: 60px;
    text-align: center;
}
h2 {
    font-size: 30px;
    text-align: left;
    position: relative;
    left: -2em;
    line-height: 0px;
    top: 8em;
}
h3 {
    font-size: 40px;
    text-align: left;
    position: relative;
    left: -0em;
    bottom: 0.2em;
}
h4 {
    text-align: center;
    position: relative;
    font-size: 25px;
    bottom: 1.2em;
}
h5 {
    font-size: 20px;
    text-align: center;
    position: relative;
    bottom: 3em;
}
</style>

# Лабораторная работа №2
## Ilyinsky A. Arseniy 
## RUDN University, 2022 Moscow, Russia

---

# Дискреционное разграничение прав в Linux

---

### Цель выполнения работы

- Получение практических навыков работы в консоли с атрибутами файлов.

- Закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux (дистрибутив - Rocky).

---

# Выполнение работы

---

### Выполнение работы

![h:100 w:800 center](images/1.png)
#### Рис.1 Создание пользователя guest

---

### Выполнение работы

![h:100 w:800 center](images/2.png)
#### Рис.2 Установка пароля для guest

---

### Выполнение работы

![w:600 center](images/3.png)
#### Рис.3 Вход в систему под guest

---

### Выполнение работы

![h:60 w:700 center](images/5.png)
#### Рис.4 Домашняя директория

---

### Выполнение работы

![h:60 w:700 center](images/6.png)
#### Рис.5 Определение пользователя

---

### Выполнение работы

![w:800 center](images/7.png)
#### Рис.6 Имя пользователя, группа, а также группы, куда входит пользователь

---

### Выполнение работы

![w:550 center](images/8.png)
#### Рис.7 Группы пользователя

---

### Выполнение работы

![h:170 center](images/9.png)

![h:88 center](images/10.png)
#### Рис.8 guest в etc/passwd

---

### Выполнение работы

![h:90 center](images/11.png)
#### Рис.9 Существующие в системе директории

---

### Выполнение работы

![h:75 center](images/12.png)
#### Рис.10 Расширенные атрибуты

---

### Выполнение работы

![h:41 center](images/13.png)

![h:115 center](images/14.png)
#### Рис.11 Права доступа к новому файлу 

---

### Выполнение работы

![h:110 center](images/15.png)
#### Рис.12 Изменение аттрибутов

---

### Выполнение работы

![h:61 center](images/16.png)

![h:56 center](images/17.png)
#### Рис.13 Запись в файл без прав

---

### Выполнение работы

![h:450 center](images/24.png)
#### Рис.14 Минимально необходимые права для выполнения операций внутри директории dir1

---

# Вывод

---

# Спасибо за внимание