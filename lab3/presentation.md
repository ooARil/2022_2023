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

# Лабораторная работа №3
## Ilyinsky A. Arseniy 
## RUDN University, 2022 Moscow, Russia

---

# Дискреционное разграничение прав в Linux. Два пользователя

---

### Цель выполнения работы

- Получение практических навыков работы в консоли с атрибутами файлов для нескольких пользователей.

- Закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux (дистрибутив - Rocky).

---

# Выполнение работы

---

### Выполнение работы

![w:1200 center](images/4.png)
#### Рис.1 Создание пользователя guest2

---

### Выполнение работы

![w:1000 center](images/5.png)
#### Рис.2 Добавление пользователя guest2 в группу guest

---

### Выполнение работы

![w:1000 center](images/6.png)
![w:1000 center](images/7.png)
#### Рис.3 Вход в консоль от пользователя guest и guest2

---

### Выполнение работы

![w:1000 center](images/8.png)
![w:1000 center](images/9.png)
#### Рис.4 Нахождение пользователей guest и guest2

---

### Выполнение работы

![w:1000 center](images/10.png)
![w:1000 center](images/11.png)
#### Рис.5 Определение пользователей

---

### Выполнение работы

![w:1200 center](images/12.png)
#### Рис.6 Группа, а также группы, куда входит пользователь guest

---

### Выполнение работы

![w:1200 center](images/13.png)
#### Рис.7 Группа, а также группы, куда входит пользователь guest2

---

### Выполнение работы

![w:1200 center](images/16.png)
#### Рис.8 Группы пользователя guest

---

### Выполнение работы

![w:1200 center](images/17.png)
#### Рис.9 Группы пользователя guest2

---

### Выполнение работы

![w:1200 center](images/18.png)
![w:1200 center](images/19.png)
#### Рис.10 Вывод команды cat /etc/group

---

### Выполнение работы

![w:1200 center](images/22.png)
#### Рис.11 Регистрация пользователя guest2 в группе guest

---

### Выполнение работы

![w:1000 center](images/23.png)
#### Рис.12 Изменение прав на директории пользователя guest

---

### Выполнение работы

![w:1000 center](images/30.png)
#### Рис.13 Минимально необходимые права для выполнения операций внутри директории dir1

---

# Вывод

---

# Спасибо за внимание