# Overview
1. Request will come from the browser
2. It will go to MongoExpress Extrenal service
3. Then it will go to MongoExress Pod (Pod will connect to internal service of MongoDB)
4. Then the request will forward to MongoDB pod
5. MongoDb will authenticate request using credentials


# Steps:
1. Install minikube:    
    curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
    sudo install minikube-linux-amd64 /usr/local/bin/minikube

2. Create mongodb deployment

3. Create mongodb secrets file

4. Apply mongodb-secret file and then mongodb-deployment file

5. Create mongodb internal service

6. Create mongo-express deployment

7. Cretae a config map is a external configuration so that their is a centralise way to use this configmap by other components

8. Apply mongo-comfigmap file and then mongo-express-deployment file

9. Create mongo-express external service

# Application Flow

Request come form DB ---> Mongo-express external service ---> mongo-express-pod ---> Mongodb-internal service ---> mongodb-pod