## Docker 

    docker exec -it 9b73e17453e3 bash 

    docker cp ./my2.sql 9b73e17453e3:/tmp 

    mysql --user=root -p < tmp/my2.sql

    mysql -Uroot -p mysql2 


https://github.com/meob/my2Collector