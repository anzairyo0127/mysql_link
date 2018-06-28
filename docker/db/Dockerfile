# イメージ「mysql:8.0.11」導入 
FROM mysql:8.0.11

RUN echo "!includedir /etc/mysql/mysql.conf.d/" >> /etc/mysql/my.cnf

COPY mysql.conf.d/mysqld.cnf /etc/mysql/mysql.conf.d/mysqld.cnf
