## RabbitMQ

RabbitMQ with default definitions.

- Ports:
-- 15672 for administration
-- 5672 for consumers

Update the `definitions.json` file to suit your needs.

Docker-compose:
```
version: "3.7"
services:
  rabbit:
    image: rafamdd/rabbitmq
    ports:
      - 15672:15672
      - 5672:5672
```

More info: https://www.rabbitmq.com/