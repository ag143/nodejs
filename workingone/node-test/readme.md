working node-js
https://node-app-service1-ag143.cloud.okteto.net/create

1) create docker image based on dockerfile
2) docker build -t node-test .
3) docker tag node-test ag143/node-test
4) docker push ag143/node-test
5) kubectl create deployment --image ag143/node-test node-app
6) kubectl expose deployment node-app --type=NodePort --port 8080
or 
 kubectl expose deployment node-app --type=LoadBalancer --port 5050
