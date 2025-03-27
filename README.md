install wsl on windown powershell
wsl --install
wsl -l -v


Redis installation command 

curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list

sudo apt-get update
sudo apt-get install redis

sudo service redis-server start

redis-cli

Redis link: https://github.com/microsoftarchive/redis/releases/tag/win-3.2.100
github link :https://github.com/jangalianand/spring-redis 

--connection pool
application.properties
---------------------------------------
Database Connection Properties

spring.application.name=student

server.port=9090
spring.datasource.url=jdbc:mysql://localhost:3306/test
spring.datasource.username=root
spring.datasource.password=****
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
#spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect


HikariCP settings
spring.datasource.hikari.connection-timeout=20000
spring.datasource.hikari.maximum-pool-size=10
spring.datasource.hikari.minimum-idle=5
spring.datasource.hikari.idle-timeout=300000
spring.datasource.hikari.pool-name=HikariCP
spring.datasource.hikari.max-lifetime=600000

Logging settings
logging.level.com.zaxxer.hikari.HikariConfig=DEBUG
logging.level.com.zaxxer.hikari=TRACE

MapStruct is a Java-based code generation tool used in Spring Boot and other Java applications to simplify the mapping between Java bean types. It helps in reducing the boilerplate code that developers typically write when converting one type of object to another. In the context of Spring Boot, you can use MapStruct to map DTOs (Data Transfer Objects) to entities or vice versa, which is a common requirement when building RESTful APIs or web applications.
MapStruct is a Java-based code generation tool commonly used in Spring Boot applications to simplify and automate the mapping of data between different Java bean types, such as DTOs (Data Transfer Objects) and entities

