# Using CloudFormation To Deploy a web server on EC2

In this demo, we will be deploying a Linux web servera using CloudFormation template. 
 
 
### Prerequisites

You need an AWS account. Set up a Free-Tier account www.aws.amazon.com/free.
 
### Let’s have fun!

#### Step 1: Prepare the CloudFormation Template
 
 - Create a JSON or YAML file 

#### Step 2:  Create an EC2 instance

- First, you must create a SSH key pair in the EC2 console. 

- Once you have a key pair you can access, go to the cloudformation console. 

- Click create stack. 

- Upload a new template. 

- Name your stack. Mine will be demo.

- Fill out the form. There are three parameters: 

    - instance type  (select t2.micro for free tier) 
    
    - key name (select the one we created earlier) 
    
    - SSH location (leave it all open for now)
    
- Click next. 

- Leave everything as default and click next. 

- Under the options sections, 

. And then click create stack. While the stack is being created, let us review the events. Before the instance can be created, the security group has to be created. And that is why you are seeing that the security group creation is complete. Now the web server itself is being created. I'll continue to refresh to see any updates. And now, the web server creation has been completed and the stack has moved to a create complete state. We can now check under resources to confirm that both the web server and the security group have been completed. And lastly, we can review the output. We will open the website URL in a new tab. This can sometimes happen because the web server takes a few seconds to boot up and start running. Let's give it a few seconds and try again. And you can see that our web server is now up and running.