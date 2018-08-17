FROM ubuntu:xenial-20180705
MAINTAINER TIGER

RUN apt-get update && apt-get install -y apache2
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
