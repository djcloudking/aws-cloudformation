## Lab: Creating and updating cloudformation stacks

### 1. Create an EC2 instance with a security group for SSH access

- Log in to AWS account

- Go to CloudFormation dashboard



- Create CloudFormation using template ***1-ec2-template.yml***

- 



### 2. Attach an EBS volume to the EC2 instance, retaining original resources

- Click on the stack you just created.

- Go to **Resources** 

- Click on **Change set**, then **Create Change Set**

- Select **Replace Existing template**, then **Update a template file**

- Upload ***2-ec2-template.yml***

- Verify the results


### 3. Add an Amazon S3 bucket to the setup, retaining all previous resources

- Do same as above (in 2.) but Upload ***3-ec2-template.yml***

- Verify the results.

