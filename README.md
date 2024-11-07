# Kafka commands
Enter in kafka's container
```SHELL
docker exec -it fc2-gokafka-kafka-1 bash
```
Create a new topic
```SHELL
kafka-topics --create --topic=test --bootstrap-server=localhost:9092 --partitions=3
```
Create a new consumer
```SHELL
kafka-console-consumer --topic=test --bootstrap-server=localhost:9092
```
Execute Go main function
```SHELL
go run cmd/producer/main.go
```
After running these commands, you should expect a "message" being shown at the kafka's consumer that you just created
