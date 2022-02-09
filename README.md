# kubernetes-flask-mysql

## Install docker 
https://docs.docker.com/engine/install/ubuntu/

## installation of minikube on my Ubuntu


``` shell
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

To install Minikube on other OS: https://minikube.sigs.k8s.io/docs/start/

To verify the minikube version, use the command: *minikube version*

To Start your cluster: from a terminal with administrator access (but not logged in as root), 
Do not forget to run: *minikube start 

To avoid any driver issue: you can run *sudo minikube start --driver=none*

## Creation of a Secret to keep the password for the Database

View the secret.yaml

## Creation of the (Persistent Volume ) PV and the PVC ( Claim)

View the persistent-volume.yml 

## Deploy the MySQL server

View the mysql-deployment.yml

Deploying the Mysql Server: ``` kubectl apply -f mysql-deployment.yml ```

And see if a pod is running via ``` kubectl get pods ```.

## Create database and table

``` shell
kubectl run -it --rm --image=mysql --restart=Never mysql-client -- mysql --host mysql --password=<clear_password>
```

``` sql
CREATE DATABASE DS3;
USE DS3;
CREATE TABLE weapons(weapon_id INT PRIMARY KEY AUTO_INCREMENT, weapon_name VARCHAR(255), weapon_name_fr VARCHAR(255), weapon_category VARCHAR(255));

SHOW DATABASES;
SHOW TABLES;
```
