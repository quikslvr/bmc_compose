1. import code dir to docker-compose root directory, as BusinessModelComposer
2. build and start project #docker-compose up -d
3. import database dump #docker exec -i db mysql -uroot -proot bmc < path_to_dump/db.sql
