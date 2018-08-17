FROM ubuntu:xenial-20180705
MAINTAINER TIGER

RUN apt-get update && apt-get install -y apache2

RUN chgrp -R 0 /var && \
    chmod -R g=u /var

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
