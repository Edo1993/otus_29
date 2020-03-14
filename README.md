# otus_29
# mysql

# Домашнее задание

Развернуть базу из дампа и настроить репликацию.
В материалах приложены ссылки на вагрант для репликации и дамп базы bet.dmp. Базу развернуть на мастере и настроить, чтобы реплицировались таблицы:

| bookmaker |

| competition |

| market |

| odds |

| outcome

* Настроить GTID репликацию

варианты которые принимаются к сдаче
- рабочий вагрантафайл
- скрины или логи SHOW TABLES
* конфиги
* пример в логе изменения строки и появления строки на реплике

_____________________________________________________________________________________________________________________________

Проверка:

Vagrantfile поднимаем ```vagrant up```. На мастере:
```
USE bet;
INSERT INTO bookmaker (id,bookmaker_name) VALUES(1,'1xbet');
SELECT * FROM bookmaker;
```
![Img_alt](https://github.com/Edo1993/otus_29/blob/master/291master.png)

На слейве:

![Img_alt](https://github.com/Edo1993/otus_29/blob/master/291slave.png)

![Img_alt](https://github.com/Edo1993/otus_29/blob/master/292.png)
