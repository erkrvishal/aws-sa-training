FROM ubuntu:latest
MAINTAINER Vishal
RUN apt update -y && apt install apache2 -y
RUN service apache2 start
COPY index.html containercat.jpg /var/www/html/
ENTRYPOINT ["apache2ctl", "-D", "FOREGROUND"]
EXPOSE 80

