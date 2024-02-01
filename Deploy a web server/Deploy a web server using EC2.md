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

- Under the options sections, click create stack. 

- Go back to the created stack and review the events. 

- Double check if the security group creation is complete, then the webserver itself. 

- Refresh and now ypou should see that the web server creation has been completed and the stack has moved to a create complete state. 

- Go to the output,open the website URL in a new tab. Now you can see that our web server is now up and running. If not,  give it a few seconds and try again. 