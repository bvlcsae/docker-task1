FROM alpine:3.9
COPY ./php-5.6.27.tar.gz /usr/local
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories \
    && apk update \
    && apk add build-base  && apk add tar \
    && cd /usr/local \
    && tar -zxvf php-5.6.27.tar.gz && cd php-5.6.27

CMD echo "This is a test."