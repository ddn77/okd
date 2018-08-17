FROM ubuntu:xenial-20180705
MAINTAINER TIGER

RUN apt-get update && apt-get install -y apache2

### Setup user for build execution and application runtime

ENV HTTPD_PREFIX /usr/local/apache2
ENV PATH $HTTPD_PREFIX/bin:$PATH
RUN mkdir -p "$HTTPD_PREFIX" \
	&& chown www-data:www-data "$HTTPD_PREFIX"

WORKDIR $HTTPD_PREFIX

EXPOSE 80
    
### Containers should NOT run as root as a good practice


CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
