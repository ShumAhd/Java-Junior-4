# Java Junior (семинары)
## Базы данных и инструменты взаимодействия с ними
Выполнить задание на СУБД h2
1. С помощью JDBC выполнить:
 
   1.1 Создать таблицу book с колонками id bigint, name varchar, author varchar, и т.д.

   1.2 Добавить в таблицу 10 книг

   1.3 Сделать запрос select from book where author = 'какое-то имя' и прочитать его с помощью ResultSet
 

2. С помощью JPA(Hibernate) выполнить:

   2.1 Описать сущность Book из пункта 1.1

   2.2 Создать Session и сохранить в таблицу 10 книг
 
   2.3 Выгрузить список книг какого-то автора

## Фйлы кода

[Class Book](https://github.com/ShumAhd/Java-Junior-4/blob/main/src/main/java/org/example/Book.java
) 

представляет структуру данных для хранения информации о книге и включает необходимые методы для работы с этой информацией при использовании Hibernate.

[Class JdbcExample](https://github.com/ShumAhd/Java-Junior-4/blob/main/src/main/java/org/example/JdbcExample.java) 

представляет собой пример использования JDBC для взаимодействия с базой данных H2. 
Создания таблицы, добавления данных и выполнения выборки из базы данных H2.


[Сlass JpaExample](https://github.com/ShumAhd/Java-Junior-4/blob/main/src/main/java/org/example/JpaExample.java) 

представляет собой пример использования Java Persistence API (JPA), конкретно Hibernate, для взаимодействия с базой данных H2, включая создание сущности, сохранение данных и выполнение выборки.

[persistence.xml](https://github.com/ShumAhd/Java-Junior-4/blob/main/src/main/resources/META-INF/persistence.xml)

Этот XML-файл представляет собой конфигурацию для Java Persistence API (JPA), используемого с Hibernate для взаимодействия с базой данных H2, с определенной сущностью Book и настройками подключения к базе данных H2.

[pom.xml](https://github.com/ShumAhd/Java-Junior-4/blob/main/pom.xml)

Представляет собой файл конфигурации Maven, известный как Project Object Model (POM), который описывает проект и его зависимости

## Результаты запуска кода

[Class JdbcExample](https://github.com/ShumAhd/Java-Junior-4/blob/main/src/main/java/org/example/JdbcExample.java)

`Book: id=5, name=Book 5, author=Author 5`

[Сlass JpaExample](https://github.com/ShumAhd/Java-Junior-4/blob/main/src/main/java/org/example/JpaExample.java)

```
Book: Book{id=1, name='Book1', author='Author1'}
Book: Book{id=3, name='Book3', author='Author1'}
Book: Book{id=5, name='Book5', author='Author1'}
Book: Book{id=7, name='Book7', author='Author1'}
Book: Book{id=9, name='Book9', author='Author1'}
```


