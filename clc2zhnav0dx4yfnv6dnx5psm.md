# How to use AWS EC2, EBS, and S3 services using AWS CLI…

***In which blog we know about how to use ec2,ebs and s3 services using AWS CLI…***

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949342204/F6RUVJAp-.jpeg)

**How to use AWS EC2, EBS, and S3 services using AWS CLI…**

**What is AWS CLI?**

AWS Command Line Interface (AWS CLI) is an open-source tool that enables you to interact with AWS services using commands in your command-line shell. With minimal configuration, the AWS CLI enables you to start running commands that implement functionality equivalent to that provided by the browser-based AWS Management Console from the command prompt in your terminal program.

### Step-1. Download AWS CLI software from this website.

click on the Windows and download.

After installation open cmd and type the command:- ***aws — version***

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949343478/Ip7lq-MEX.png)

### Step-2. Now we need to configure aws…..

*so firstly we can create IAM user in AWS. follow this steps:*

a) Go to AWS console.

b) Search IAM service.

c) Go to users.

d) click on the Add users.

e) give the name.

f) select Accesskey…next

g) select AdministratorAccess….next

h) click on the create user.

i) now successfully created.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949345318/pPjqvENJo.png)

**click on theIAM service.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949346765/C4tBKNQGM.png)

**click on the users.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949348645/qvea9XJw8.png)

**click on the Add users.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949350129/R_d6KbXqP.png)

**give the name.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949352212/5j6MHGdzC.png)

**select policy.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949353737/dElt660KL.png)

**create user.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949355095/f_0wctOFr.png)

successfully created.

### Step-3. We need to login AWS CLI using Accesskey ID and Secret access key.

**Download the .csv file………**

Go to cmd and type ***aws configure*** command.

a) copy IAM user ***Access key ID*** and ***Secret access key.*** and paste in cmd

b) give the ***region name*** where you want to launch your instance.

c) give the output format…like ***Json.***

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949356542/i4goKeMTe.png)

### Step-4. We will launch Amazon EC2 Instance using AWS CLI.

we will launch ec2 instance with the help of this command…..

a) you can take any image-id from AWS console.

b) you can use existing key-pair.

c) you can use any existing security-group-id.

d) you can use any existing subnet-id.

f) every id belong to same availablity zone.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949358537/FBYnGg2d8.png)

Now Sucessfully Launch EC2 Instance.

### Step-5. We will Create Key-pair using AWS CLI.

*Using this command create Key-pair.*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949361196/MQNdHz_c5.png)

Give the key-pair name.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949362977/aeek3w0Ye.png)

Now successfully created.

### Step-6. We will Create EBS Volume using AWS CLI.

*using this command create EBS Volume.*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949364555/VHi2aTIHf.png)

Now Sucessfully Created.

### Step-7. We will attach EBS volume to EC2 Instance using AWS CLI .

*using this command attach EBS Volume to EC2 Instance.*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949366126/pAb02FuXN.png)

### Step-8. We will create Security Group using AWS CLI.

*a) use this command :-* **aws ec2 create-security-group — group-name my-sg — description “My security group” — vpc-id vpc-1a2b3c4d**

b) vpc id :- You can find vpc from here → goto VPC services → click on VPCs

Now we have successfully created a security group in Amazon EC2.

### Step-9. We will create S3 Bucket using AWS CLI.

a) Upload an object to S3 bucket use command :- ***aws s3 cp object\_name s3://bucketname***

b) use this command :- ***aws s3api put-object-acl — bucket (bucketname) — key (object-name) — acl-public-read.***

Now we can access the object publicly.

### Step-10. We will find commands in AWS CLI.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949367953/f65vHjQK8.png)

using this command.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949369501/eaFqh6lOE.png)

**Thank you so much for reading, I hope this is helpful for you.**

[Ajaydhangar](https://medium.com/u/51e2e016e988)