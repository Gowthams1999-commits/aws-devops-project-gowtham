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
Block Public Access Settings: By default, AWS blocks all public access to S3 buckets for security. If you want to allow public access to your bucket, you can adjust this setting.
### Bucket Versioning: Optional. You can enable versioning to keep track of different versions of your objects.
Tags: Optional. You can add metadata tags for organizing or tracking the bucket.
### Encryption: You can enable encryption to automatically encrypt the files that are uploaded to the bucket.

### 6. Configure Bucket Permissions (Optional)
Permissions: You can add or manage permissions for specific users, groups, or roles. By default, S3 uses Access Control Lists (ACLs) and IAM policies to control access to the bucket.

### 7. Review and Create
After filling out all necessary fields, click the Create bucket button at the bottom of the page.

### 8. Bucket Created
Once the bucket is created, you'll be redirected to the Buckets list where you can see your newly created bucket. 
