# Micro Services Eureka Server (Discovery Server)
will be responsible for communication across different microservices (clients)
Each microservice will register itself in this server then it will be available for other microservices


# prerequisites
config server should be up and run<br/>
<a href="https://github.com/JavaAdore/config-server">https://github.com/JavaAdore/config-server</a>

# EUREKA_SERVER_PORT=8761
8761 ia default port of eureka-server, but it could be replaced with any unused port

the following environment variables should be presented
# CONFIG_SERVER_IP = 127.0.0.1 
127.0.0.1 will be used if config server is running on the same machine of eureka-server

# build
as root/Administration <br/>
mvn clean install docker:removeImage docker:build
# run
java -jar target/eureka-server.jar

# browse
<a href="http://127.0.0.1:8761">http://127.0.0.1:8761</a>



