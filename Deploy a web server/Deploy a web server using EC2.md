# Using CloudFormation To Deploy a web server on EC2

In this tutorial, we will be deploying a simple AWS S3 bucket using the previously discussed CloudFormation template. 
 
 Background
 
 
 
 Prerequisites
 
 Let’s have fun!

 Step 1: Prepare the CloudFormation Template
 
 - Create a JSON or YAML file 

 Deploy a web server using EC2
Selecting transcript lines in this section will navigate to timestamp in the video
- [Instructor] In this demo, we will deploy a Linux web server using the previously discussed template. In this case, we will be creating a EC2 instance. So to follow along, you must create a SSH key pair in the EC2 console. Once you have a key pair you can access, go to the cloud formation console. Just like the previous demo, we will upload a new template. I will name this stack demo as well. Now we have three parameters. We can choose the instance type. Remember how we were expecting it to be a dropdown, so it is. I'm going to leave it as a M3 medium. Under the key name, I have one key name already created so I will select that. And then for SSH location, I will just leave it all open for now as this is a website and just going to be up for a few minutes. Click next. I will leave everything as default and click next. You can now check the options. And then click create stack. While the stack is being created, let us review the events. Before the instance can be created, the security group has to be created. And that is why you are seeing that the security group creation is complete. Now the web server itself is being created. I'll continue to refresh to see any updates. And now, the web server creation has been completed and the stack has moved to a create complete state. We can now check under resources to confirm that both the web server and the security group have been completed. And lastly, we can review the output. We will open the website URL in a new tab. This can sometimes happen because the web server takes a few seconds to boot up and start running. Let's give it a few seconds and try again. And you can see that our web server is now up and running.