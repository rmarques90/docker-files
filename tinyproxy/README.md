## Tinyproxy

Docker-compose example:
``` 
version: "3.7"
services:
  app:
    image: rafamdd/tinyproxy
    ports:
      - 8888:8888
    volumes:
      - type: bind
        source: ./tinyproxy.conf
        target: /etc/tinyproxy/tinyproxy.conf

```