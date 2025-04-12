03/04/2025
deployment will configure in the yaml file for pod and replica set>
(for deployment and replicaSet apiVersion is apps/v1)
apiVersion: apps/v1
kind: Deployment
metadata:
  name: blue-deploy
  namespace: blue-ns
spec:
  replicas: 5
  selector:
    matchLabels:
      app: ipl
  template:
    metadata:
      labels:
        app: ipl
    spec:
      containers:
        - name: c-1
          image: daviddocker526/ipl-srh:latest
          ports:
            - containerPort: 80

--------------------
killercoda free labs:
killercoda login through google
kubectl get nodes

--------------------
ec2 instance:
sudo su
kubectl create ns blue-ns
kubectl get ns
vi blue-deployment.yaml
cat blue-deployment.yaml
kubectl apply -f blue-deployment.yaml
kubectl get deployment -n blue-ns
kubectl get rs -n blue-ns
kubectl get pods -n blue-ns
kubectl describe pod blue-deploy-8568d84476-6zbg5 -n blue-ns

vi blue-service.yaml

apiVersion: v1
kind: Service
metadata:
  name: blue-service
  namespace: blue-ns
spec:
  selector:
    app: ipl
  ports:
    - protocol: TCP
      port: 80
      targetPort:
  type: LoadBalancer



1)clusterip(to expose app on each worker node)
2)nodeport
3)load balancer(provides external ip )(to access application out of the cluster)
4)external name(to map domain name)

cat blue-service.yaml

kubectl apply -f blue-service.yaml
kubectl get all -n blue-ns

(killercoda doesn't provide loadbalancer it is a paid service...so it will show pending...)
in the website check the external ip address

kubectl delete pod blue-deploy-8568d84476-54b85 -n blue-ns
kubectl get pods -n blue-ns
  
(in yaml file ..replicas:1 )
vi blue-deployment.yaml
kubectl apply -f blue-deployment.yaml
kubectl get pods -n blue-ns


(to allow editing in yaml file opened ...to be able to insert any characters...press "i"....then start editing..)
kubectl get all -n blue-ns
kubectl delete deployment blue-deploy -n blue-ns
kubectl delete svc blue-service -n blue-ns
------------------------------------------------------------------------------
Jenkins:
to automate the application deployment....(in Kubernetes we did manual eployment)
it is a ci/cd(delivery and deployment) tool..
plugin is a piece of software...tool will be available in the form of plugins....we install plugins..


ec2 instance
t3 medium
select existing group default
20 gb launch instance
security:
enable port 22 ->all tcp save rules

in putty:
paste the ip address
browse  and upload key pair..

sudo su
apt update -y


Jenkins install on ubuntu os in website
linux->ubuntu
long term support
copy and paste

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

press y

once Jenkins is installed ..install java too..
same website.....
installation of java

sudo apt update
paste all code snippets

java --version

start Jenkins:
copy the commands
start the Jenkins server(it wil take time)
port of Jenkins is 8080
check the status

give public ip address of ec2 instance ...past it in new tab with  the port :8080(access only through web)
copy the location and do the cat command
cat ***(path)
paste the passpord in web..and continue..
install suggested plugins....
(it will take time)
(then create a pipeline)
create first admin
give any password
 and provide all details....save and continue..start Jenkins..
manage Jenkins
->plugins->available pluggins->

1.	AWS Credentials
2.	Kubernetes Client API
3.	Kubernetes CredentialsVersion
4.	Kubernetes
5.	Kubernetes CLI
6.	Kubernetes Credentials Provider
7.	Kubernetes :: Pipeline :: DevOps Steps
install all these plugins ...in the Jenkins web server..
login with new credentials ...or eskle we will get HTTP ERROR 403 NOT FOUND....
how to provide aws access keys..
create aces keys in ec2 instance in security groups and let it download..
manage Jenkins..
credentials under security
system ->global credentials.  add credentials ->aws credentials...provide id and description:anything
paste th access key id...click on create
how to get kubeconfig files from Jenkins server..
execute the commands as mentioned int the word document sent by sir...
refer the word documenrt for the clear steps..
install kubectl install on ubuntu os...install(Kubernetes)...copy the commands..
install unzip software...

install unzip -y

install awscli on ubuntu os...
aws configure then paste the key.specify the region...none....
execute the elastic kubernetes service...there we can find the cluster name...
commands to copy the kubeconfig name to Jenkins server....then execute the rest of the commands..switch as Jenkins user....sudo su -Jenkins..
then again provide access keys ...using the commands..aws configure...
then save the kubeconfig file as document..follow the command....then do ....ls...use cat..
using cat config..

go to jenkins sever..add global security credentials and then add the file..the kubeconfig file is added..
dashboard  all new item ....pipeline..add
pipeline....write the script...copy the script..
copy the eks script from "stage ...."(2 snippets)
save and apply..click on pipeline server..git Git...give a repo url for it......update git inside "git:..."
....

ec2 instance..
kubectl get all


in pipeline..build now....click on the loading output...it will give the entire history...
generate script for another component..and paste it...
Then deploy the application.....
refer the document..
------------------------------------------------------------------
