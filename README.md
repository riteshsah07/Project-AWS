# Project-AWS
Topic : Building an Auto-Scaling Cloud Architecture for Streaming Platforms
Project Overview:
🔹 Automated EC2 Instance Creation – Developed a Launch Template to automatically spin up EC2 instances.
🔹 Auto-Scaling Group Implementation – Ensured seamless traffic management by distributing loads across multiple EC2 replicas.
🔹 Live Demo Deployment – Accessed the public IPv4 address of the dynamically created instance to showcase our working application.
🔹 Performance Testing with BlazeMeter – Evaluated website performance under high traffic, ensuring scalability and resilience.


# Step for building an Auto-Scaling Cloud Architecture for Streaming Platforms
Step 1 : First We have created an Launch Template which automatically creates EC2 and
required templates.
Basically we have use an static website as a Demo to perform and test our performance and check for the load management.
Step 2: We have created an autoscaling group so that the traffic on the page could be distribute across the replica of the EC2 instance .To help in distribute traffic across the network Load Balancer is automatically applied to the Auto Scaling group.
Step 3: After creating Auto Scaling Group we have navigate to EC2 which was created ,click on the EC2 and copied the public IPV4 address and paste it to the browser with port 8080 which was 54.162.70.49:8080 (8080 is a communication endpoint that web servers use to listen for incoming requests). 
Step 4: Finally we have check the performance of the site through BlazeMeter.

