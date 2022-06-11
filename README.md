```
윈도우 환경에서는 git bash로 curl를 쉽게 할수있다.

```


# Start the application
export DEBEZIUM_VERSION=1.8
docker-compose -f docker-compose-jdbc.yaml up

# Start PostgreSQL connector
curl -i -X POST -H "Accept:application/json" -H  "Content-Type:application/json" http://localhost:8083/connectors/ -d @pg-sync.json

# Start MySQL connector
curl -i -X POST -H "Accept:application/json" -H  "Content-Type:application/json" http://localhost:8083/connectors/ -d @mysql-sync.json