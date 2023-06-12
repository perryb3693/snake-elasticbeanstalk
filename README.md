# tomcat-elasticbeanstalk
The purpose of this repository is to deploy the "Tomcat" game on AWS Elastic Beanstalk. Tomcat is "a snake game where you collect points by eating food". Source files for the Tomcat game can be found at: https://github.com/chandradeoarya/tomcat-jsp-snakegame

***Step One: Create an AWS Elastic Beanstalk environment with Java platform and Tomcat as the application server***
First, copy project files to the working directory
```
git clone https://github.com/chandradeoarya/tomcat-jsp-snakegame.git
```
Initialize elasticbeanstalk and set the default values to run a java application using Tomcat. 
```
eb init
```
Configurations:
- Select your default region of choice
- Create a new application
- Enter application name or use default
- Select Java as platform
- Select Corretto 17 as platform branch
- Setup SSH to allow remote management of instances and choose/create keypair

Create a new environment to deploy to Elastic Beanstalk
```
eb create eb-snake --single     #"--single" option creates an environment with a single EC2 instance and without a load balancer
```

***Step Two: Test the Tomcat game by visiting the Elastic Beanstalk environment URL***
(EB-Environment-Domain)/webapp 

Example Format: http://eb-snake2.eba-z2uhcpip.ca-central-1.elasticbeanstalk.com/webapp


