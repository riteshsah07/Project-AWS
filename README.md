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
User Data we have use for the launch template.
# !/bin/bash
sudo apt-get update -y
sudo apt-get install -y openjdk-11-jdk maven git tomcat10 tomcat10-admin
# Create a directory for your application
sudo mkdir -p /opt/myapp
cd /opt/myapp
# Clone the GitHub repository
sudo git clone https://github.com/anujdevopslearn/MavenBuild.git
cd MavenBuild
# Build the Maven project
sudo mvn clean install
# Deploy the WAR file
sudo cp target/myapp.war /var/lib/tomcat10/webapps/
# Start Tomcat
sudo systemctl start tomcat
We have added 3 Security Rule in the Add Security Group Rule and Created a Security Group.
1.Custom TCP with port range 8080-8089 and source type Anywhere( 0.0.0.0/0)
2.SSH with port 22 and source type Anywhere(0.0.0.0/0)
3.HTTP with port 80 and source type Anywhere(0.0.0.0/0)
Basically we have use an static website as a Demo to perform and test our performance and check for the load management.
Step 2: We have created an autoscaling group so that the traffic on the page could be distribute across the replica of the EC2 instance .To help in distribute traffic across the network Load Balancer is automatically applied to the Auto Scaling group.
Step 3: After creating Auto Scaling Group we have navigate to EC2 which was created ,click on the EC2 and copied the public IPV4 address and paste it to the browser with port 8080 which was 54.162.70.49:8080 (8080 is a communication endpoint that web servers use to listen for incoming requests). 
Step 4: Finally we have check the performance of the site through BlazeMeter.

