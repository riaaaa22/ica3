This repo deploy a Wordpress stack along with a Proxy sever in a Kubernetes cluster with the database.
Steps for working this application in your Kubernetes Cluster:

# STEP1 
Clone the repo in your local kubernetes cluster or GKE 

**git clone https://github.com/PiyushTyagi-Tech/containerisation-ica2.git**

# STEP2
Creating the required namespaces:

**kubectl create namespace wp-app**

**kubectl create namespace mariadb**

**kubectl create namespace nginx-proxy** 

# STEP3
Applying the changes to all the services and Deployment in the cluster

**kubectl apply -f <.yaml - files >**

**_eg mariadb deployment and services files in directory mariadb: kubectl apply -f deployment.yaml_**

# STEP4
Accessing the application from loadbalancer service in nginx-Service EXTERNAL IP.

# _OPTIONAL_STEP5 

if using the local cluster use modify the **LoadBalancer** type service (nginx-service.yaml)in nginx-proxy namespace to  **NodePort**



