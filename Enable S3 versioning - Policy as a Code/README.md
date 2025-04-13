****Enforce S3 Versioning Policy – Ansible Playbook****

This Ansible playbook enables versioning on all existing S3 buckets in your AWS account.

**What It Does**

1. Lists all S3 buckets using amazon.aws.s3_bucket_info

2. Enables versioning using amazon.aws.s3_bucket



