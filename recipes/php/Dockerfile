FROM registry.centos.org/che-stacks/centos-stack-base

MAINTAINER Madalin Ignisca <madalin.ignisca@yahoo.com>

EXPOSE 8080

LABEL che:server:8080:ref=php che:server:8080:protocol=http

COPY mariadb.repo /etc/yum.repos.d/mariadb.repo

RUN sudo yum update -y && \
    sudo yum -y localinstall https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm \
      https://rpms.remirepo.net/enterprise/remi-release-7.rpm && \
    sudo yum-config-manager --enable remi-php72 && \
    sudo yum -y install composer \
      gcc-c++ make \
      MariaDB-client \
      nano \
      php-bcmath \
      php-cli \
      php-gd \
      php-gmp \
      php-intl \
      php-json \
      php-mbstring \
      php-mysqlnd \
      php-opcache \
      php-pdo \
      php-pgsql \
      php-snuffleupagus \
      php-sodium \
      php-twig \
      php-xml && \
    sudo yum -y clean all
