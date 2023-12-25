# Block 1
## Команды для запуска
```
docker-compose build 
docker-compose up -d 
docker-compose up -d (почему-то на маке с m1 пришлось еще раз выполнить)
docker-compose exec kafka kafka-topics.sh --bootstrap-server kafka:9092 --create --topic itmo2023 --partitions 1 --replication-factor 1
docker-compose exec kafka kafka-topics.sh --bootstrap-server kafka:9092 --create --topic itmo2023_preprocessed --partitions 1 --replication-factor 1
docker-compose exec jobmanager ./bin/flink run -py /opt/pyflink/device_job.py -d
python3.11 producer_1.py
python3.11 consumer_1.py
```
Сделал только первый пункт с local dir.
# Block 2
Команды для запуска те же самые, только используем другие джобы с соответсвующими названиями
