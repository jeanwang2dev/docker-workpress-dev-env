# MYSQL
FROM mysql:5.7.26

ENV MYSQL_ROOT_PASSWORD simple_psw
ENV MYSQL_DATABASE demo_wp_db
ENV MYSQL_USER demowpuser
ENV MYSQL_PASSWORD simple_psw

# wordpress basic sql to start with
# MYSQL will import the sql file at startup
 COPY demo_wp_db.sql /docker-entrypoint-initdb.d/