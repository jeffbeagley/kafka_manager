# Kafka Manager
I was getting tired of running curl commands from a CLI for Kafka Connect configurations, so I decided to make a quick UI to handle the process for me. I welcome recommendations and pull requests for any added functionality.

![alt text](https://s3.amazonaws.com/beagley-misc/Screenshot+from+2018-12-20+17-06-43.png)

### Current Functionality
- View, and Create Topics
- View, Create, Delete Kafka Connectors
- View, Create, Manage, and Execute KSQL

### Current Todos
- Return Server Status
- Allow Pause/Resume of individual Tasks
- Allow Topic Deletion

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Docker build
```
npm run build-docker
```

### Run Docker
```
docker run -it -d -e PORT=9500 -p 9500:9500 kafka_manager:latest node server.js
```

## Run on Kubernetes
#### In order to run on K8, you need to setup an ingress that the App can hit from outside of K8
### Apply yaml file
```
kubectl apply -f k8.yaml
```

## Environment Variables
```
PORT: nodejs port to run nodejs from
VUE_APP_CONNECT_SERVER: hostname for Kafka Connect instance
VUE_APP_REST_SERVER: hostname for Kafka REST Api
VUE_APP_KSQL_SERVER: hostname for Kafka KSQL 
