FROM php:8.1.7-fpm

RUN curl -L https://download.newrelic.com/php_agent/release/newrelic-php5-10.0.0.312-linux.tar.gz | tar -C /tmp -zx && \
  export NR_INSTALL_USE_CP_NOT_LN=1 && \
  export NR_INSTALL_SILENT=1 && \
  /tmp/newrelic-php5-*/newrelic-install install && \
  rm -rf /tmp/newrelic-php5-* /tmp/nrinstall* && \
  docker-php-ext-install opcache && \
  mkdir /app
