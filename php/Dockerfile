FROM alpine:3.3

# Patch APK Mirror to YKode
RUN echo "https://mirrors.ustc.edu.cn/alpine/v3.3/main" > /etc/apk/repositories

# ENV TIMEZONE Asia/Shanghai
# ENV PHP_MEMORY_LIMIT 512M
# ENV MAX_UPLOAD 50M
# ENV PHP_MAX_FILE_UPLOAD 200
# ENV PHP_MAX_POST 100M

RUN apk update && \
    # apk add tzdata && \
    # cp /usr/share/zoneinfo/${TIMEZONE} /etc/localtime && \
    # echo "${TIMEZONE}" > /etc/timezone && \
    apk add php-intl \
    php-mcrypt \
    php-openssl \
    php-gmp \
    php-json \
    php-dom \
    php-pdo \
    php-zip \
    php-zlib \
    php-mysqli \
    php-bcmath \
    php-gd \
    php-xcache \
    php-pdo_mysql \
    php-gettext \
    php-xmlreader \
    php-xmlrpc \
    php-bz2 \
    php-memcache \
    php-iconv \
    php-curl \
    php-ctype \
    php-fpm \
    php-phar \
    php && \
    mkdir /www && \
    # apk del tzdata && \
    rm -rf /var/cache/apk/*

WORKDIR /www
# VOLUME ["/www"]

EXPOSE 9000
CMD ["php-fpm"]

# FROM alpine:3.9
# COPY ./php-5.6.27.tar.gz /usr/local
# RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories \
#     && apk update \
#     && apk add tar \
#     && cd /usr/local \
#     && tar -zxvf php-5.6.27.tar.gz && cd php-5.6.27 \
#     && apk add gcc gcc-c++ libxml2 libxml2-devel libjpeg-devel libpng-devel freetype-devel openssl-devel libcurl-devel libmcrypt-devel

# WORKDIR /usr/local/php-5.6.27

# CMD echo "This is a test."
# docker stop $(docker ps -aq)
# docker rm $(docker ps -a | grep "Exited" | awk '{print $1 }')
# docker rmi $(docker images | grep "none" | awk '{print $3}')
# docker rm $(docker ps -aq)
# docker run -itd --name myphp1 php1
# docker attach myphp1