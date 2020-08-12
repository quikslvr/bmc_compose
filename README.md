1. import code dir to docker-compose root directory, set code dir name to .env file as CODE_DIR variable
2. set database credentials in to path_to_code_dir/app/config/parameters.yml
   - database_host: db
   - database_port: null
   - database_name: bmc
   - database_user: root
   - database_password: bmc
3. build and start project #docker-compose up -d
4. run composer install #docker exec -i fpm ./composer.phar install
5. import database dump #docker exec -i db mysql -uroot -pbmc bmc < path_to_dump/db.sql
6. set 127.0.0.1 example.com in to /etc/hosts
