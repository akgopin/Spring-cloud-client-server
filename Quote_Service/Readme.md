The server is a spring boot cloud client micro service server connecting to 
config_service_server running on http://localhost:8888 for property fetch during start up.

If property value for an environment need to be changed lets say dev, 

step 1: The user need to modify the dev properties file configured for the "app name" in git and commit the same.

The "app name" is configured in bootstrap.properties spring.application.name=Product_Service

step 2: To reflect the change on the client micro service invoke the below end point
POST http://localhost:8080/refresh

This will call the server and refresh the configuration values
