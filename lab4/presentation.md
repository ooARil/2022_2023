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

# Лабораторная работа №4
## Ilyinsky A. Arseniy 
## RUDN University, 2022 Moscow, Russia

---

# Дискреционное разграничение прав в Linux. Расширенные атрибуты

---

### Цель выполнения работы

- Получение практических навыков работы в консоли с расширенными атрибутами файлов.

- Закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux (дистрибутив - Rocky).

---

# Выполнение работы

---

### Выполнение работы

![w:1500 center](images/1.png)
#### Рис.1 Определение расширенных атрибутов файла file1

---

### Выполнение работы

![w:1500 center](images/2.png)
#### Рис.2 Установление прав на файл file1

---

### Выполнение работы

![w:1500 center](images/3.png)
#### Рис.3 Установление расширенных прав на файл file1 пользователем guest

---

### Выполнение работы

![w:1500 center](images/4.png)
#### Рис.4 Установление расширенных прав на файл file1 суперпользователем

---

### Выполнение работы

![w:1500 center](images/5.png)
#### Рис.5 Проверка расширенных прав на файл file1

---

### Выполнение работы

![w:1500 center](images/6.png)
#### Рис.6 Выполнение дозаписи в файл с атрибутом a

---

### Выполнение работы

![w:1500 center](images/7.png)
![w:1500 center](images/8.png)
#### Рис.7 Удаление и перезапись файла с атрибутом a

---

### Выполнение работы

![w:1500 center](images/9.png)
#### Рис.8 Изменения прав на файл с атрибутом a

---

### Выполнение работы

![w:1500 center](images/10.png)
![w:1500 center](images/11.png)
#### Рис.9 Повторение операций без атрибута a

---

### Выполнение работы

![w:1500 center](images/13.png)
![w:1500 center](images/14.png)
#### Рис.10 Повторение операций с атрибутом i

---

# Вывод

---

# Спасибо за внимание