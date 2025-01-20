## Lab: Creating and updating cloudformation stacks

### 1. Create an EC2 instance with a security group for SSH access

- Log in to AWS account

- Go to CloudFormation dashboard

![image](https://github.com/user-attachments/assets/f4b6cf83-59b5-4ac9-b8fb-e5d778c3f321)


- Create CloudFormation using template ***1-ec2-template.yml***

 ![image](https://github.com/user-attachments/assets/4aa9aa94-1023-4da0-840d-ec601e2b8896)


### 2. Attach an EBS volume to the EC2 instance, retaining original resources

- Click on the stack you just created.

- Go to **Resources**

![image](https://github.com/user-attachments/assets/b863c136-adaa-43d0-9bda-42cb11195790)


- Click on **Change set**, then **Create Change Set**

![image](https://github.com/user-attachments/assets/7a21d814-727e-4bbc-8e0f-f8753513272b)


- Select **Replace Existing template**, then **Update a template file**

![image](https://github.com/user-attachments/assets/55656138-a1bc-4739-8dd1-3430669259f4)


- Upload ***2-ec2-template.yml***

- Verify the results

![image](https://github.com/user-attachments/assets/2ad83a5b-d4b3-4554-9c4b-d142c4979e6e)


![image](https://github.com/user-attachments/assets/138f2919-973e-426c-b7dd-6fbcce6eac3d)


![image](https://github.com/user-attachments/assets/29a8d838-d8b5-4aa3-babb-de32f1941c31)


### 3. Add an Amazon S3 bucket to the setup, retaining all previous resources

- Do same as above (in 2.) but Upload ***3-ec2-template.yml***

![image](https://github.com/user-attachments/assets/bfc35262-92c4-48bc-bce1-bd2789d80753)


- Verify the results.

  ![image](https://github.com/user-attachments/assets/df8cd29d-2901-44ba-89e8-1a1430842537)


  ![image](https://github.com/user-attachments/assets/55fc5e96-951f-4b47-9eae-82ff3f738d6b)
  



