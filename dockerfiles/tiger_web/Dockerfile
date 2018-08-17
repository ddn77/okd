FROM ubuntu:xenial-20180705
MAINTAINER TIGER

RUN apt-get update && apt-get install -y apache2

### Setup user for build execution and application runtime
ENV APP_ROOT=/var

RUN chmod -R u+x /usr/sbin && \
    chgrp -R 0 ${APP_ROOT} && \
    chmod -R g=u ${APP_ROOT} /etc/passwd

### Containers should NOT run as root as a good practice
USER 10001
WORKDIR ${APP_ROOT}

RUN chgrp -R 0 /var && \
    chmod -R g=u /var

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
