# Cost Optimization
In this document, we will explore cost optimization in AWS using Lambda Functions. We will use Lambda functions to delete stale objects from AWS in order to avoid extra charges.

Let's assume we have created an EC2 instance and are running a customer application on it. The customer wants to take a snapshot of the EC2 instance every day. We are taking snapshots using the EBS volume and Snapshot feature. After a few months, the customer wants to stop the application on the EC2 instance and halt the EC2 instance service. They raise a request to delete the EC2 instance. As the DevOps engineer deletes the EC2 instance but forgets to delete the snapshots, AWS will continue to charge for the running services, even though they are no longer in use.

In this scenario, we will create a Lambda function to identify all volumes associated with EC2 instances and fetch all snapshot details.

If a volume is no longer associated with an instance, its corresponding snapshot will be deleted. I have created Python code to identify volumes and snapshots, filter inactive or stale objects, and delete them.


