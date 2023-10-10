# Mongo-local + WEB-UI
add .env:
```
DB_USERNAME="<dbusername>"
DB_PASSWORD="<dbpassword>"
MONGOUI_USERNAME="<uiusername>"
MONGOUI_PASSWORD="<uipassword>"
```
```The database and UI will be created using these credentials```<br><br>
```
docker compose --env-file=.env up --build
```
Access to DB by UI: http://localhost:8081

Access to DB from terminal:
```
docker exec -it local-mongodb mongosh -u <dbusername> -p <dbpassword> --authenticationDatabase admin
```
Access to DB from any app outside docker container:
```
mongodb://<dbusername>:<dbpassword>@localhost:8080
```
There is a problem with admin rights. Discussed here:

https://github.com/mongo-express/mongo-express/issues/809
