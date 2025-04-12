******************************Docker**************************************8

Git Bash:
mkdir microservices-app
cd
ls -ll
ls -l
mkdir order_service
mkdir user_service
touch filenames

cat > file : to write
cat file : to display
nano file: open
ctrl+X and Y and enter: to save

*****************************Kubernetes Architecture****************************

-Orchestration Platform:
-To manage containers
-is an orchestration platform for containers
-Kubernetes will  use Docker internally, using K8S we will manage our Docker containers.

Docker Swarm vs K8S:
-Docker Swarm doesn't have auto scaling(scaling is manual process)
-K8S supports auto scaling
-Kubernetes is replacement for Docker Swarm

Cluster:
-Group of Servers
-Master Node(s)
-Worker Node(s)
-DevOps Engineer/Developer will give the task to K8S Master Node
-Master Node will manage worker nodes
-Master Node will schedule tasks to worker nodes
-Our containers will be created in worker nodes
-using cluster we can achieve high availability

*****************************Kubernetes Architecture**********************************8

-Control Plane/Master Node/Manager Node: Responsible to handle K8S related work
	-API server
	-Scheduler 
	-Control Manager 
	-ETCD

-Worker Node(s): Responsible to execute our application as PODS
	-Pods
	-Containers
	-Docker engine
	-kubelet: worker node agent, maintain al the info related to worker node
	-kube proxy: Provide network K8S cluster communication(MN->WN)
	-docker runtime

*******************************************Kubernetes Cluster Setup**********************************

1. Self Managed Cluster(We will create our own cluster)
a. Mini Kube (Single Node Cluster)
b. Kubeadm(Multi Node Cluster)

2. Provider Managed Cluster (Cloud Provider will give ready made Cluster)--->Charges applies
a. AWS EKS
b. Azure AKS
c. GCP GKE

**************************************Cluster creation AWS*******************************************

EKS
Kubernetes Architecture:
Kubernetes 
	Orchestration platform
	To manage containers
	Developed by Google using Go language
	Google donated K8S to CNCF
	K8S first version released in 2015
	It is free and open source
 1  kubectl --version
    2  curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.24.11/2023-03-17/bin/linux/amd64/kubectl
    3  chmod +x ./kubectl
    4  sudo cp ./kubectl /usr/local/bin
    5  export PATH=/usr/local/bin:$PATH
    6  kubectl --version
    7  kubectl version
    8  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
    9  unzip awscliv2.zip
   10  sudo ./aws/install
   11  ~
   12  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
   13  unzip awscliv2.zip
   14  sudo ./aws/install
   15  git --version
   16  sudo yum install git -y
   17  git --version
   18  git clone https://github.com/N4si/K8s-voting-app.git
   19  ls
   20  cd k8s-voting-app aws
   21  cd k8s-voting-app
   22  cd K8s-voting-app
   23  ls
   24  cd ..
   25  kudectl ge nods
   26  kubectl get nods
   27  aws eks update-kubeconfig --name shree-cluster --region us-east-1
   28  aws configure
   29  aws eks update-kubeconfig --name shree-cluster --region us-east-1
   30  kubectl get nodes
   31  history

