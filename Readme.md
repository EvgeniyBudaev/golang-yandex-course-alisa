Библиотека для тестирования testify
```
go get -u github.com/stretchr/testify
```

Клиентская http библиотека
```
go get -u github.com/go-resty/resty/v2
```

Логирование
```
go get -u github.com/sirupsen/logrus
```
```
go get -u go.uber.org/zap 
```

Пакет gomock. Имитация данных для тестирования
```
go get -u github.com/golang/mock/mockgen@latest
```
Абстрактный интерфейс и SQL-драйверы
Установка MySQL
```
go get -u github.com/golang/mock/mockgen@latest
```
# далее нужно установить настройки безопасности
```
mysql_secure_installation
```
Установка PostgreSQL
```
sudo apt -y install postgresql
```
[Здесь](https://winitpro.ru/index.php/2019/10/25/ustanovka-nastrojka-postgresql-v-windows/){target="_blank"} вы найдёте
подробную инструкцию по установке PostgreSQL на Windows,
а [здесь](https://ruvds.com/ru/helpcenter/postgresql-pgadmin-ubuntu/){target="_blank"} — на Linux Ubuntu.
[Здесь](https://wiki.postgresql.org/wiki/Russian/PostgreSQL-One-click-Installer-Guide){target="_blank"} —
инструкция по установке на macOS.

Итак, вы установили СУБД. Чтобы начать с ней работать, нужно создать базу данных. Воспользуемся консольным клиентом
`mysql` для MySQL и MariaDB, а также `psql` — для PostgreSQL.

Вот пример создания БД PostgreSQL на Linux:
```
sudo -i -u postgres
psql -U postgres
postgres=# create database dbname;
postgres=# create user username with encrypted password 'userpassword';
postgres=# grant all privileges on database dbname to username; 
```

Для подключения к СУБД PostgreSQL с помощью драйвера
```
go get -u github.com/jackc/pgx/v5
```