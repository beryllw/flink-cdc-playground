# MySQL CDC to Kafka Demo

1. Setup Kafka using Docker Compose(docker-compose.yml )
2. Start the Kafka Cluster( docker-compose up -d)

```bash
docker-compose up -d   

docker-compose ps

docker-compose exec kafka kafka-topics.sh --create --topic baeldung_linux
  --partitions 1 --replication-factor 1 --bootstrap-server kafka:9092
  
docker-compose exec kafka kafka-console-consumer.sh --topic baeldung_linux
  --from-beginning --bootstrap-server kafka:9092

docker-compose exec kafka kafka-console-producer.sh --topic baeldung_linux
  --broker-list kafka:9092
```