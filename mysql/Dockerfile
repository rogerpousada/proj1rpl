FROM mysql:5.7

ADD my.cnf /etc/mysql/conf.d/my.cnf
RUN chown -R mysql:root /var/lib/mysql/
#COPY schema.sql /docker-entrypoint-initdb.d/
COPY database_schema.sql /docker-entrypoint-initdb.d/

#ARG MYSQL_DATABASE=notes
#ARG MYSQL_USER=notes-api
#ARG MYSQL_PASSWORD=notes-api
#ARG MYSQL_ROOT_PASSWORD=root

#ENV MYSQL_DATABASE=$MYSQL_DATABASE
#ENV MYSQL_USER=$MYSQL_USER
#ENV MYSQL_PASSWORD=$MYSQL_PASSWORD
#ENV MYSQL_ROOT_PASSWORD=$MYSQL_ROOT_PASSWORD

CMD ["mysqld"]
EXPOSE 3306
