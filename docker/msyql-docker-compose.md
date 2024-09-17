__Spring booot side__
```yml
spring:
  application:
  name: candinates-services

  datasource:
    url: jdbc:mysql://localhost:3306/candidate
    username: root
    password: 1234
  jpa:
    hibernate:
      ddl-auto: update
    properties:
      hibernate:
        dialect: org.hibernate.dialect.MySQLDialect

```
__Mysql__
----

```yml
version: "3.8"

services:
  mysql-server:
    container_name: mysql
    image: mysql
    ports:
      - "3306:3306"
    environment:
      MYSQL_ROOT_PASSWORD: 1234
      MYSQL_DATABASE: candidate
      MYSQL_USER: ogleh
      MYSQL_PASSWORD: 12345
      volumes:
         - datadb:/var/lib/mysql/data

volumes:
  datadb
  