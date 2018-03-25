The server is a spring boot cloud config server connecting to a remote git hub
repository https://github.com/akgopin/spring-cloud-config

The server is stateless

http://localhost:8888/Product_Service/default - will retrieve the default configurations for the application
application with "app name" Product_Service

http://localhost:8888/Product_Service/dev - will retrieve the configurations for dev environment.

For each request the server clones a copy of the requested resource