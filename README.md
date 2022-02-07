# kubernetes-flask-mysql

# installation of minikube on my ubunutu 

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

sudo install minikube-linux-amd64 /usr/local/bin/minikube

To install Minikube on other OS: https://minikube.sigs.k8s.io/docs/start/

To verify the minikube version, use the command: minikube version

To Start your cluster: from a terminal with administrator access (but not logged in as root), 
# Do not forget to run: # minikube start

# Creation of a Secret to keep the password for the Database

View the secret.yaml

# Creation of the (Persistent Volume ) PV and the PVC ( Claim)

View the persistent-volume.yml 

# Deploy the MySQL server
