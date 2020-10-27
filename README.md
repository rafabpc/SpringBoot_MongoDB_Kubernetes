
# How to Run

## 1 - Build the APP

```mvn clean compile install```


## 2 - Build the APP docker image

```docker build -f Dockerfile -t application-example:1.0 .```


## 3 - Run the Kubernetes YAML files

```kubectl apply -f mongodb-example-config.yaml```

```kubectl apply -f mongodb-example-deployment.yaml```

```kubectl apply -f application-example-deployment.yaml```

## 4 - Check the status of your services
```kubectl get services```

```kubectl get pods```

## 5 - Executing the application

```@see Postman Collection (SpringBootMongoDBKubernetesCollection.postman_collection.json)```


## 6 - Opening the MongoDB in MongoDBCompass

```mongodb://<your-ip-address>:27017/mongodb-example```


# Tests
The application is covered by unit and integration tests, the covarage can be seen in jacoco.

```target > site > jacoco > index.html```


# Docker
The configuration for Docker can be seen in:

```Dockerfile```

# Kubernetes
The configuration for Kubernetes can be seen in:

```mongodb-example-config.yaml```

```mongodb-example-deployment.yaml```

```application-example-deployment.yaml```


# MongoDB
The configuration for MongoDB can be seen in:

```src > main > resources > application.properties```

```mongodb-example-config.yaml```

```mongodb-example-deployment.yaml```
