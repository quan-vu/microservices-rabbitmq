# Microservices with RabbitMQ

Microservices skeleton on Docker using RabbitMQ for asynchronous IPC support Python &amp; Golang.

**TODO**

* [x] Setup simple Microservice on Docker using RabbitMQ
* [x] Create a service skeleton with Flask
* [x] Create a service skeleton with Go
* [x] Sample for handle inter-process communication (IPC)
* [ ] Implement business transactions using Microservices use Saga Pattern
* [ ] Create a service skeleton with FastAPI


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

## References

Thanks to nice articles:

- [Microservices & RabbitMQ On Docker](https://dev.to/usamaashraf/microservices--rabbitmq-on-docker-e2f)

- [Saga Pattern | How to implement business transactions using Microservices – Part I](https://blog.couchbase.com/saga-pattern-implement-business-transactions-using-microservices-part/)