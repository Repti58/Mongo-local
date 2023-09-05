# Mongo-local + WEB-UI
add .env:
```
DB_USERNAME="<dbusername>"
DB_PASSWORD="<dbpassword>"
MONGOUI_USERNAME="<uiusername>"
MONGOUI_PASSWORD="<uipassword>"
```
```
docker compose --env-file=.env up --build
```
Access DB by UI:

http://localhost:8081

Access to db from terminal:
```
docker exec -it local-mongodb mongosh -u <dbusername> -p <dbpassword> --authenticationDatabase admin
```
Access db from any app outside docker container:
```
mongodb://<dbusername>:<dbpassword>@localhost:8080
```
