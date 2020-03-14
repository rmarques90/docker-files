FROM alpine
RUN set -xe \
 apk update && \ 
 apk add --update --no-cache tinyproxy
COPY ./tinyproxy.conf /etc/tinyproxy
EXPOSE 8888
CMD ["tinyproxy", "-d"]