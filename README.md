# docker-compose-files
Some basic common docker-compose files helpful in development.

### Accessing Kafka from your localhost
You need to add "127.0.0.1 kafka" (or whatever you give in kafka.yml) to /etc/hosts in order to access Kafka from your local machine.

#### kafka.yml
KAFKA_CFG_ADVERTISED_LISTENERS=PLAINTEXT://kafka:9092

### Troubleshoot
If containers give "permission denied" errors when creating folders, try this in data folder:

> sudo chown -R 5050:5050 pgadmin/

> sudo chmod 777 zookeper/ kafka /

You can use Kafka [Offset Explorer](https://www.kafkatool.com/) to play with Kafka.
