Web Browser
Web server
App Server

What is Horizontal and vertical scaling?
Vertical: increase the number of CPU s
Horizontal: automatically increase the number of servers

1.Load balancer---->to distribute the incoming application traffic to registered targets called servers.
2.Autoscaling---->Automatically add or remove servers based on traffic and defined policy.
3.Cloud watch alarms---->will trigger the alarm when there is a problem in servers, whenever crossed the CPU utilization threshold.
4.SNS-Simple notification Service---->Sends notification to the registered emails.

Elastic Load Balancing(ELB)
-Automatically distributes traffic across multiple targets
-Provides high availability
-Incorporates security features
-Performs health checks

3 types of Load balancer
-Application Load Balancer
-Network Load Balancer 
-Gateway Load Balancer

Load Balancer

Amazon EC2 Auto Scaling
-Helps you control EC2 instances available to handle the load for your application
-Launches or terminates your AWS resources based on specified conditions
-Registers new instances with load balances with load balancers, when specified.

