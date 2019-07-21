FROM nginx:stable-alpine
COPY ./html /src
RUN rm -rf /usr/share/nginx/html && \
    chown -R nobody:nobody /src && chmod -R 775 /src && \
    mv /src /usr/share/nginx/html
