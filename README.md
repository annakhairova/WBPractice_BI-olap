### Локальная сборка

docker build -t postgre13 .

### Запуск контейнера

docker run -d \
  --name postgres \
  --restart unless-stopped \
  --memory 512m --cpus 1.0 \
  -p 5432:5432 \
  -v ./postgres:/data/postgres \
  postgre13

### Перезапуск контейнера

docker restart postgres

### Удаление контейнера

docker rm -f <ID или имя контейнера>


### Для Compose

docker-compose up -d

docker-compose up <имя_контейнера>

#### Сборка перед запуском

docker-compose up --build