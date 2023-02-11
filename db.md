# DB

```sh
# installation mariadb
[toto@db ~]$ sudo dnf install mariadb-server
[sudo] password for toto:
Last metadata expiration check: 1:42:26 ago on Fri Feb 10 10:10:55 2023.
Dependencies resolved.
```

```sh
# mise en route du service
[toto@db ~]$ sudo systemctl enable mariadb
Created symlink /etc/systemd/system/mysql.service → /usr/lib/systemd/system/mariadb.service.
Created symlink /etc/systemd/system/mysqld.service → /usr/lib/systemd/system/mariadb.service.
Created symlink /etc/systemd/system/multi-user.target.wants/mariadb.service → /usr/lib/systemd/system/mariadb.service.
[toto@db ~]$ sudo systemctl start mariadb
[toto@db ~]$ systemctl status mariadb
● mariadb.service - MariaDB 10.5 database server
     Loaded: loaded (/usr/lib/systemd/system/mariadb.service; enabled; vend>
     Active: active (running) since Fri 2023-02-10 11:55:21 CET; 30s ago
       Docs: man:mariadbd(8)
```

```sh
[toto@db ~]$ sudo mysql_secure_installation

# said yes to everything
```

```sh

```


```sh
MariaDB [(none)]> CREATE USER 'api'@'10.107.1.12' IDENTIFIED BY 'toto';
Query OK, 0 rows affected (0.011 sec)

MariaDB [(none)]> CREATE DATABASE IF NOT EXISTS groupie CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
Query OK, 1 row affected (0.000 sec)

MariaDB [(none)]> GRANT ALL PRIVILEGES ON groupie.* TO 'api'@'10.107.1.12';
Query OK, 0 rows affected (0.012 sec)

MariaDB [(none)]> FLUSH PRIVILEGES;
Query OK, 0 rows affected (0.000 sec)
```

```sh
```

```sh
```

```sh
```

```sh
```

```sh
```

```sh
```

```sh
```

```sh
```
