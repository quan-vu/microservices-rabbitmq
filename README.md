# Microservices with RabbitMQ

Microservices skeleton on Docker using RabbitMQ for asynchronous IPC support Python &amp; Golang.

## Test it

Start python service on docker

```
$ cd microservices-rabbitmq
$ docker exec -it microservices-rabbitmq_python-service bash
# root@62fa0cbb4d35:/python-service# 

# Run Flask application
FLASK_APP=main.py python -m flask run --port 3000 --host 0.0.0.0
```

Start go service on docker

```
$ cd microservices-rabbitmq
$ docker exec -it microservices-rabbitmq_go-service bash
# root@ede84d6b4e7e:/go-service# 

# Run go application
go run main.go
```

Start a client on new termial

```
$ curl -d "full_name=David" -X POST http://localhost:3000/users/1
# {"full_name":"David"}
```

Open sevice's terminal you will see the update.