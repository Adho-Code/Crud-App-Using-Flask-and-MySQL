FROM	ubuntu:latest

RUN		apt update && \
	apt install mysql-server -y

ENV MYSQL_ROOT_PASSWORD 1 
ENV MYSQL_DATABASE my_db 
ENV MYSQL_USER simon
ENV MYSQL_PASSWORD demopass123
EXPOSE  3306

CMD ["mysqld"]
