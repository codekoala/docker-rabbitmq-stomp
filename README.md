# docker-rabbitmq-stomp
A Dockerfile to run [RabbitMQ](https://www.rabbitmq.com/) clusters (with the [STOMP plugin](https://www.rabbitmq.com/stomp.html) enabled) using Kubernetes.

This Dockerfile is based [on nanit's RabbitMQ image](https://hub.docker.com/r/nanit/rabbitmq/) so exported ports and volumes defined by it should also apply.

## DockerHub
https://hub.docker.com/r/codekoala/rabbitmq-stomp/

## Using

See https://github.com/codekoala/kubernetes-rabbitmq-cluster

Exposed ports:

+ 4369  => RabbitMQ epmd (port mapper for clustering)
+ 5671-5672  => RabbitMQ default node port (transport)
+ 15672 => RabbitMQ web management (http access)
+ 25672 => RabbitMQ inter-node communication (clutering)
+ 61613 => RabbitMQ STOMP broker port (transport)
