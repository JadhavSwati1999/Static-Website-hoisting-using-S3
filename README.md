
# Static website hosting using S3 bucket

## What is S3 bucket in AWS

Amazon simple storage service (Amazon S3) is an object storage service that offers industry leading scalability data availability security and performance .

You can use Amazon S3 to store and retrieve any amount of data at any time , from anywhere.

S3 bucket is vision specific , it looks like a global service but bucket are created in a region.

   

## Why S3 is used

S3 offers :

- Leading scalability
- Data availability
- Security and performance
- Disaster recovery
- Backup and storage
- Archive
- Static website
- Media hoisting
- Application hoisting
- Hybrid cloud storage

## How to host static website using S3 bucket

## **Step 1: Logging In to the Amazon Web Services Console**

login to your AWS account using your credentials.

## **Step 2:** **Step 2: Creating an Amazon S3 Bucket for a Static Website**

1. In the AWS Management Console search bar, enter S3, and click the S3 result under Services:

2. To start creating a new Amazon S3 bucket,  click Create bucket:        


3. Under General configuration, enter the following: Bucket name: Enter
• Region: Ensure US East(N. Virginia) us-east-1 is selected


1. In block all public access:


5.In the Block Public Access section, un-check the Block all public access check box:

6. To acknowledge that you want to make this bucket publicly accessible, check I acknowledge that the current settings might result in this bucket and the objects within becoming public:



7. To finish creating your Amazon S3 bucket, scroll to the bottom of the form and click Create bucket:


## **Enable static website hosting for your bucket:**

8. In the list, click the name of your bucket:

9. To upload objects click on upload ,in the top-right:


1. You can drag and drop files and folders here: 


1. Once all the files are ready to upload:


1. Click on upload:



13.All the files are uploading into S3 bucket


14. In the row of tabs under Bucket overview, click Properties:


1. Edit static website hoisting ,enable static website:
- add your main html page with .html extension



1. Click on Save changes: 


17.In the row of tabs under Bucket overview, click Permission:


1. Edit bucket policy:


1.  Click on ,Generate policy:
- AWS Policy Generator

Step 1: Select Type of Policy - S3 Bucket Policy

- Add Statement(s)
1. Effect - Allow
2. Principle - *(all)
3. Actions - select the action(GetObject)
4. Copy and add the ARN of your bucket


1. Click on Generate Policy


1. Policy is generated , policy JSON Document 
- Copy the JSON document and paste it into the Bucket Policy



1. Copy the URL that is generated at the time you enable static website :
- Paste the domain name into the address bar of a new browser tab.
- you will get the output.


# Summary

In this project you created a S3 Bucket ,and enabled the host static website, generated the Bucket Policy, from which we got a json document ,paste the domain name into the browser tab. This is how we hosted a static website using  AWS S3 Bucket.