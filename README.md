This Repository tells about AWS CloudFormation to create and manage S3 buckets and using Stack Drift Detection to monitor changes. 

Scenario 1
1.Create S3 Bucket using CFT:
2.Imported a YAML file to create an S3 bucket.
3.Deployed the YAML file, resulting in the creation of the bucket.
4.Deleted the bucket manually (not via CloudFormation).

Check Stack Drift:
1.Used Stack Drift Detection to check for changes.
2.Stack Drift Detection reported that the bucket was deleted.

Scenario 2
1.Create S3 Bucket with Versioning using CFT:
2.Imported a YAML file with versioning configuration enabled.
3.Deployed the YAML file, resulting in the creation of the bucket with versioning enabled.
4.Manually disabled versioning on the bucket.

Check Stack Drift:
1.Used Stack Drift Detection to check for changes.
2.Stack Drift Detection reported that versioning was disabled.

Benefits of Stack Drift Detection
Change Tracking: Easily identify changes to resources that were not made through CloudFormation, ensuring the integrity of your infrastructure as code.
Compliance: Helps in maintaining compliance by ensuring that all changes are tracked and managed through CloudFormation.
Quick Troubleshooting: Facilitates quick identification of issues caused by manual changes to resources.
