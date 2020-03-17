## Tinyproxy

For production use I strongly recommend to use BasicAuth in the cfg. The syntax is: `BasicAuth user password`

To validate the proxy, use `curl -x http://<proxy-host>:<proxy-port> --proxy-user <proxy-user> http://<url-to-request>`. It will prompt to enter the proxy password.

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
