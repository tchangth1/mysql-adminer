# mysql-adminer
##this is the description
version: '3.3'
services:
  mysqlsrv:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: "1234password"
      MYSQL_DATABASE: "testdb"
    ports:
      - "3306:3306"
    volumes:
      - dbdata:/var/lib/mysql
    networks:
      - mysqlnetwork

  adminer:
    image: adminer
    ports:
      - 8080:8080
    networks:
      - mysqlnetwork

networks:
  mysqlnetwork:
    driver: bridge
volumes:
  dbdata:
  
 http://ip-addr:8080
 login as root password is 1234password and server mysqlsrv and database testdb
