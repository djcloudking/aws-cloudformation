# Using CloudFormation to Deploy a simple S3 bucket

 In this short tutorial, I will be deploying a simple AWS S3 bucket using a CloudFormation template. 
 
### Prerequisites

You need an AWS account. Set up a Free-Tier account www.aws.amazon.com/free.

### Let’s have fun!

#### Step 1: Prepare the CloudFormation Template
 
 - Create a JSON or YAML file 
 
Cheat Sheet: See the attached file S3.template for a cloudformation template

#### Step 2: Connect to CloudFormation Servers

- Log in to your AWS account. 

- Go to the CloudFormation dashboard. 

- Click on create stack. 

- Select template is ready. 

- Specify where the template is located. Select the template file. 

- Click next. Put a stack name. 

This is the unique name given to every CloudFormation stack. I'm going to use the simple name demo and click next. 

- Now it gives us some additional options. First is the ability to specify some tags. Just to demonstrate this, I will create a stack with a tag purpose and value demo. 

- Leave the other advanced features as default. Then click next. 

- Click on create stack. Now the demo stack creation has been completed.


#### Step 3: Verification and test

- Select the stack and review its details. For example, stack ID, events that took place in creation of the stack, resources, outputs of the stack. 

- Go under the S3 and confirm that a new S3 bucket has been created. You can see that a new bucket now exists with the name demo S3 bucket. This confirms that our stack was created successfully.


#### Step 4: Ve

- Remember that our original goal was to have a website. Let's try to achieve that. I'm at the CloudFormation service console. I will open the stack named demo, go into output and try to open the website URL in a new tab. Notice that I got a 404 error. If you review the error message, it is trying to find the file index.html but unable to find it. Why is it looking for that file? Let's go back to the console and review the template. It is looking for that file because we specified index.html as the index document. We have not uploaded the index.html or the error.html file. So let us do that. We will go into the S3 servers. Go to our bucket. Click upload. Select our files by browsing to them. And hit open. Click next. Just leave everything as default. And both the files have been uploaded. Now we can go back to the website tab and hit refresh. The 404 error has now been replaced by a 403 error. We know that is is related to permissions and what we are missing is a bucket policy. Let's upload a new template which specifies the bucket policy. Go back to the CloudFormation console. Click on demo. Update, we will replace the current template with a new template that we will be uploading. So click choose file, choose the new template and click next. Just leave everything else default. At the review console, you can see that is showing that there is one change being made. That is a new bucket policy, my bucket policy, is being added. We will click update stack. While the stack is being updated, let us review the new template. In addition to having the S3 bucket resource, we now have a new resource called my bucket policy. This is a S3 bucket policy which attaches itself to the bucket with the logical name S3 bucket. And the policy effectively specifies that any file in this S3 bucket can be read by any user, thus making it a public website. Notice how the update is now complete. If we go to the website tab and hit refresh, we now have a static website. You can continue to add files to turn it into a complete website.