Storage options in AWS:
-------------------------------
1. object storage:s3(simple storage service)
  -s3 is durable and scalable
  -s3 is pay-as-you-go
  -s3 used to upload files/images/movies/pdf files/CSV files/folder etc
  -s3 called bucket
  -s3 bucket size is 5TB, can create each account 100 buckets
  -s3 bucket can keep public and also private

When u create s3 bucket follow the steps(naming rules)
	-global unique
	-min 3 characters and max 63 characters
	-no special characters/no caps/no spaces

aws s3api create-bucket --bucket shreepai2004 --region ap-south-1 --create-bucket-configuration LocationConstraint=ap-south-1
aws s3api delete-bucket --bucket shreepai2004 --region ap-south-1


terraform init
terraform validate
terraform plan
terraform apply
terraform destroy



-----------------------------------------------------------------------------------------------------------
Docker:
create instances->connect
sudo su
yum update
yum install docker -y
docker pull ubuntu
docker images
docker image -a ---> to check the containers
docker run redis

docker run -it ubuntu   --->to go inside the containers
docker start <container_name>
docker attach <container_name>
ll --->


    1  yum update
    2  yum install docker -y
    3  docker --version
    4  service docker start
    5  docker info
    6  docker pull ubuntu
    7  docker images
    8  docker ps -a
    9  docker run redis
   10  docker images
   11  docker run alpine
   12  docker images
   13  docker ps -a
   14  docker run -it ubuntu
   15  docker images
   16  docker ps -a
   17  docker start wizardly_wescoff
   18  docker attach wizardly_wescoff
   19  docker ps -a
   20  docker ps
   21  docker start wizardly_wescoff
   22  exit
   23  history


