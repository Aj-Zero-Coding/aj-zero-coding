# How to create a s3 bucket using terraform ?

In this blog, we will first discuss the S3 bucket and then the main Terraform configuration file. We will also cover the AWS S3 object bucket in terraform.

How to create a s3 bucket using terraform ?

### 1\. Create S3 bucket module

Create a module that will have a basic S3 file configuration. For that, create one folder named **“S3,”** we will have two files: **bucket.tf and var.tf**.

### 2\. Define bucket

Open *bucket.tf* and define bucket in that.

**bucket.tf**

resource "aws\_s3\_bucket" "demos3" {  
    bucket = "${var.bucket\_name}"   
    acl = "${var.acl\_value}"     
}

*Explanation*

*   We have a block with the key name *“resource”* with resource type *“aws\_s3\_bucket”*– which we want to create. It has a fixed value, and it depends on the provider. Here we have an AWS *S3* resource where *AWS* is our provider and *S3* is our resource. *“Demos3”* is the resource name that the user provides.
*   *Bucket* and *ACL* are the argument types for our resource. We can have different arguments according to our needs and their corresponding values.
*   Either we can provide value directly or use the *var.tf* file to declare the value of an argument.

### 3\. Define variables

In *var.tf*, we will define variables for the *bucket.tf*

**var.tf**

variable "bucket\_name" {}

variable "acl\_value" {  
    default = "private"  
}

*Explanation*

*   As mentioned above, *var.tf* is used to declare values of variables. We can either provide a default value to be used when needed or ask for value during execution.

### 4\. Add Configuration

After successfully creating the S3 folder, create a file named **main.tf** for keeping configuration in our working directory.

**main.tf**

provider "aws" {  
    access\_key = "${var.aws\_access\_key}"  
    secret\_key = "${var.aws\_secret\_key}"  
    region = "${var.region}"  
}

module "s3" {  
    source = "<path-to-S3-folder>"  
    #bucket name should be unique  
    bucket\_name = "<Bucket-name>"         
}

*Explanation*

*   It contains the main set of the module’s configurations.
*   Here we provide details of our provider (AWS) and access key, secret key, etc.
*   Since we are creating S3 using terraform modules, we need to add an S3 module to create an S3 bucket. For this, we will use the keyword *“module”* and the name of the module (folder) which we have created earlier.
*   In argument, we will provide a source to the S3 module and bucket name, as we haven’t defined bucket name in *var.tf.*
*   While writing bucket name, please keep in mind that its name is unique in the region, and it does not contain “\_” or Uppercase letters.

### 5\. Add Access key, Secret key, and Region.

Now we will define *variable.tf*, where we will enter our access key, secret key, and region.

**variable.tf**

variable "aws\_access\_key" {  
default = “<your\_access\_key>”  
}  
variable "aws\_secret\_key" {  
default = “<your\_secret\_key>”  
 }  
variable "region" {  
    default = "region"  
}

*Explanation*

*   Access key, Secret key, and Region will be defined here.

We are done with creating the S3 bucket; now it’s time to set up Terraform.

### Run Terraform script in your system.

If you haven’t downloaded terraform then visit the [Terraform official document](https://www.terraform.io/downloads.html) for downloading Terraform in your system.

You can check the version of terraform installed in your machine using terraform -v command.

Run the following commands to run Terraform script in your system.

***1\. terraform init***

It is used to initialize the working directory.  
It will install the required plugins for our code, e.g., AWS S3.

You will see something like after running *terraform init* successfully-

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949277778/cddCsUK2g.jpeg)

***2\. terraform plan***

We will use this command for script verification. It will show if there is an error in our configuration.

The output of *terraform plan* looks like this if it runs successfully-

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949279750/-Z6p8k8TE.jpeg)

***3\. terraform apply***

Use *terraform apply* to create your S3 bucket.

It will ask you for confirmation before execution; enter yes for confirmation.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949281326/6lx8xL1Bu.png)

Use *terraform apply -auto-approve* if you want to execute it without asking for confirmation.

After successful execution, it will display the following message-

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949282940/VTFTlwa5V.jpeg)

You can verify your bucket in S3 services in your AWS Account.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949284323/RGU8xTWxN.jpeg)

Your Bucket will be created in the desired region.

To destroy the S3 bucket, use this command-

***terraform destroy***  
or  
***terraform destroy -auto-approve*** // if you don’t want to approve manually

After applying terraform destroy, you will see something like this-

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671949285804/1UjA-lTPC.jpeg)

So, this was about how to create an S3 bucket using Terraform.

You can find the source code- [**Github Repository.**](https://github.com/Ajay-Dhangar/s3_using_terraform)

### Conclusion

I hope this tutorial has served your purpose. For such advanced tutorials, visit our Tutorials Page and learn more about emerging technologies.

Managing DevOps needs the best and skilled experts. If you are looking for a helping hand to deploy your project or need assistance with DevOps consultation, then without a doubt, get in touch with us to work with like minded DevOps programmer. We let you hire DevOps developers from us at your ease and convenience.