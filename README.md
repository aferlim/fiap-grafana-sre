## Docker 

    docker exec -it 9b73e17453e3 bash 

    docker cp ./my2.sql 9b73e17453e3:/tmp 

    mysql --user=root -p < tmp/my2.sql

    mysql -Uroot -p mysql2 


https://github.com/meob/my2Collector


#MySQL

DROP PROCEDURE IF EXISTS ROWPERROW;
DELIMITER ;;


DELIMITER ;;
CREATE PROCEDURE ROWPERROW()
BEGIN
DECLARE n INT DEFAULT 1000000;
DECLARE i INT DEFAULT 14;
SET i=14;
WHILE i<n DO 
  INSERT INTO product(ID, name, description) Values (i, 'p', 'desc');
  SET i = i + 1;
END WHILE;
End;
;;


CALL ROWPERROW();