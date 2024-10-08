# transactional-outbox-pattern



## Open Source Kafka Startup in local ##

1. Start Zookeeper Server

    ```sh bin/zookeeper-server-start.sh config/zookeeper.properties```

2. Start Kafka Server / Broker

    ```sh bin/kafka-server-start.sh config/server.properties```

3. Create topic

    ```sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic NewTopic --partitions 3 --replication-factor 1```

## cURL to access Order Service ##

```
curl -X 'POST' \
  'http://localhost:9191/api/orders' \
  -H 'accept: */*' \
  -H 'Content-Type: application/json' \
  -d '{
  "name": "Mobile",
  "customerId": "Basant",
  "productType": "Electronics",
  "quantity": 1,
  "price": 89000
}'
```

<img width="1587" alt="image" src="https://github.com/devgitmanish/transactional-outbox-pattern/blob/main/outboxAM.png">
<img width="1587" alt="image" src="https://github.com/devgitmanish/transactional-outbox-pattern/blob/main/Screenshot%202024-09-20%20105554.png">
<img width="1587" alt="image" src="https://github.com/devgitmanish/transactional-outbox-pattern/blob/main/Screenshot%202024-09-20%20105657.png">


