What is OS?
The interface between user and hardware.

What is Cloud Computing?
Cloud Computing is nothing but on demand delivery of IT resources over the internet. You can access technical resources such as storage, databases, compute, networking, security with pay as you go.

CLOUD PROVIDERS IN MARKET: AWS, Microsoft Azure, GCP(Google Cloud Platform)

SDLC- Software Development Life-Cycle. Its a structured step by step process that development teams used to create high quality, cost effective and secure software. 

What are the server Components?
	-OS(Linux/Windows/Mac)
	-RAM(6/8/12/16 etc GB)
	-ROM(HDD/SSD)
	-NETWORKING

65.2.37.85

ls : Is a command to list files and directories, directories means folders.
touch <filename> : To create empty files. 
Ex: touch Shree
cat > Shree : to write inside the file
cat Shree : to see the content of the file
rm : delete the file 
Ex : rm Shree
mkdir : to create a directory
cd : change directory
cd ..(Exit from directory)
rmdir : to delete a empty directory
Ex: rmdir directory name
rm -r: is a command to delete directory with files
ls -l : list the files and directories with permissions
pwd : print working directory or present working directory.
history


What is DevOps?
DevOps is a set of practices, principles and cultural philosophies that aim to bridge the gap between software development and operations. 
The goal of DevOps is to shorten the software development life-cycle, improve collaboration between development and operations team and deliver high quality software faster and more efficiently.
Key elements:
-Automation
-continuous integration
-continuous delivery or requirement
-collaboration and communication
-monitoring

Waterfall Model:
It has distinct goals for each phase of development.

Traditional Waterfall model:
Requirements 
Analysis
Design
Coding
Testing
Operations

Limitations:
Once the application is in testing phase it is very difficult to go back and do changes that was not well thought out in the concept stage.

Agile/Spiral Methodology:
DevOps is a culture fostering collaboration amongst all participants involved in the development and maintenance. 
Plan
design
develop
test
display
review
launch

Develop Team: Code works in my laptop
Operation Team: There is some problem with the code it does not work in deployment.

Why DevOps matters?
DevOps is important because its a software development and operations approach that enables faster development of new products and easier maintenance of existing deployments.

Benefits:
Speed
Rapid delivery
Reliability
Improved Collaboration
Scale Security

How DevOps works?
Continuous Development - Plan Code
Continuous Testing - Build Test
Continuous Deployment
Continuous Monitoring


EC2 - Elastic Compute Cloud

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

What is a Server?
Server is a powerful computer or system that provides services or data to other computers known as clients, Over a internet.
Servers are designed to manage, store and process data and they play a critical role in handling request delivery responses within a network. 

Types of servers:
Web server: Delivers web pages to users browsers. Ex: NGINX
File server: stores and manages files that clients can access and Share over a network.
Database server: manage database and provide access to clients for reading, writing and updating data. EX: MySQL, MongoDB
Mail server: Handles the sending, receiving and storage of emails. Ex: Microsoft Exchange.

Clients 
Clients    - Internet - Server
Clients

Server components: OS, RAM, CPU, Storage, NIC(Network interface Call), ROM


EC2 Configuration:

--------------------
1. Name of the server
2. Application and OS Images (Amazon Machine Image)
        -OS selection
3. Instance type: Choose number of CPU's and RAM 
4. Keypair: used to connect securely to instance
5. Networking:
        -firewalls
	-VPS: Virtual private cloud
	-Subnets
	-route tables
	-NAT
	-Internet gateway
	-Elastic IPS
6. configure storage
	-EBS(Elastic Block store)
	-EBS nothing but similar to hard disk
	-Persistent block level storage
	-can create new volumes and attach to running instance
7. Launch instance: web server/windows server



---------------------------------------------------------------------------------------------------------------------
