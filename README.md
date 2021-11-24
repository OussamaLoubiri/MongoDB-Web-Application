# MongoDB-Web-Application-Usecase


## To run this Web application

### 1) Start Minikube
minikube start

### 2) Apply the mongodb-secret.yaml that was created with a username of admin and passowrd of password123
kubectl apply -f mongo-secret.yaml

### 3) Next deploy mongodb.yaml, during the deployment it will get the secret username and passord from the previous secret.yaml
kubectl apply -f mongodb.yaml

### 4) Apply the internal service using mongodbService.yaml to allow communication between mongodb and mongoexpress
kubectl apply -f mongodbService.yaml

### 5) Apply mongo-config.yaml for the connectivity configuration
kubectl apply -f mongo-config.yaml

### 6) Deploying MongoExpress web interface to use mongodb
kubectl apply -f mongoexpress.yaml

### 7) Applying the mongodb external service
kubectl apply -f mongo-express-external-service.yaml

### 8) Use this command to open the browser
minikube service mongo-express-external-service






