# S3 Bucket 

## Create S3 bucket

### 1. Sign in to AWS Console
Go to the AWS Management Console.

Sign in with your AWS account credentials.
### 2. Navigate to S3 Service
In the AWS Management Console, find and select S3 under the "Storage" section, or search for S3 in the search bar at the top of the console.

### 3. Create a New Bucket
On the S3 dashboard, click on the Create bucket button.

### 4. Configure Bucket Name and Region
Bucket Name: Enter a unique name for your bucket. The name must be globally unique (no other AWS user can have the same bucket name).
Example: my-unique-bucket-name
Region: Choose the AWS region where you want your bucket to be located. Pick a region that is geographically close to where your users or resources are located for better performance.
Example: US East (N. Virginia)

### 5. Set Bucket Settings
Block Public Access Settings: By default, AWS blocks all public access to S3 buckets for security. If you want to allow public access to your bucket, you can adjust this 
setting.
### Bucket Versioning: Optional. You can enable versioning to keep track of different versions of your objects.
Tags: Optional. You can add metadata tags for organizing or tracking the bucket.
### Encryption: You can enable encryption to automatically encrypt the files that are uploaded to the bucket.

### 6. Configure Bucket Permissions (Optional)
Permissions: You can add or manage permissions for specific users, groups, or roles. By default, S3 uses Access Control Lists (ACLs) and IAM policies to control access to the bucket.

### 7. Review and Create
After filling out all necessary fields, click the Create bucket button at the bottom of the page.

### 8. Bucket Created
Once the bucket is created, you'll be redirected to the Buckets list where you can see your newly created bucket. 



# Create an S3 Bucket

## Sign in to AWS Management Console:

Go to AWS Console and log in.
Navigate to S3:

From the AWS Management Console, search for S3 or find it under "Storage."
Create a New Bucket:

Click on Create bucket.
Bucket Name: Enter a globally unique name for the bucket (e.g., my-static-website-bucket).

### Important: If you want to host the website under a custom domain, use the same name as your domain (e.g., www.example.com).

### Region: Choose a region close to your audience.

### Block Public Access Settings: Uncheck the "Block all public access" option (we will allow public access for the website).
Click Create bucket.
##: Upload Website Files
Go to your S3 Bucket:

Select the bucket you just created from the S3 dashboard.
## Upload Your Static Website Files:

Click on the Upload button to upload your website files (like index.html, style.css, script.js, etc.).
Click Add files and select your website files, then click Upload.

## Configure Bucket for Static Website Hosting

### Go to the Bucket Properties:

Click on the Properties tab of your bucket.
### Enable Static Website Hosting:

Scroll down to the Static website hosting section.
Click Edit.
Select Enable for static website hosting.
Set Index and Error Document:

Index document: Enter index.html (or the name of your main HTML file).
Error document: Enter error.html (or the name of your error page, optional).
Click Save changes.

## Set Bucket Policy for Public Access
Go to the Permissions Tab:

Click on the Permissions tab of your bucket.
Edit Bucket Policy:

Scroll to the Bucket Policy section and click Edit.
Add a Bucket Policy:

To allow public access to your website files, add a policy like this (replace your-bucket-name with your actual bucket name):
json
Copy
Edit
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your-bucket-name/*"
        }
    ]
}
This policy grants read access to anyone for the objects in the bucket.

Save the Policy:

Click Save.
Step 5: Access Your Static Website
Find the Website Endpoint:

Go back to the Properties tab and find the Static website hosting section.
You will see the Endpoint URL. This is the URL where your website is hosted (e.g., http://your-bucket-name.s3-website-us-east-1.amazonaws.com).
