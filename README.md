<h1>Identity Access Management On AWS</h1>
<h3> This document presents the complete technical documentation of an end-to-end AWS Identity and Access Management (IAM) and cloud security project. </h3>
<p></p> The project demonstrates practical, hands-on proficiency across eight core AWS services   IAM, S3, EC2, CloudTrail, SNS, EventBridge, KMS, DynamoDB, and Amazon Bedrock   applied in a structured, security-first workflow that mirrors real-world cloud administration practices.

<p></p>This document presents the complete technical documentation of an end-to-end AWS Identity and Access Management (IAM) and cloud security project. The project demonstrates practical, hands-on proficiency across eight core AWS services   IAM, S3, EC2, CloudTrail, SNS, EventBridge, KMS, DynamoDB, and Amazon Bedrock   applied in a structured, security-first workflow that mirrors real-world cloud administration practices.<p></p>

<p></p>The project simulated a media organisation with four business groups   Facebook, Instagram, Threads, and IT   each with two IAM users. Beginning with root account hardening (MFA enablement), an administrative IAM user was created to avoid operating as root. The admin account was then used to provision all downstream resources: three S3 buckets and EC2 instances (one per non-IT group), with group-specific inline policies restricting each group to only their assigned resources. The IT group was granted full access to all resources across the environment.<p></p>


<p></p>An automated alerting pipeline was built using CloudTrail (for management event logging), SNS (for email notification), and EventBridge (to trigger an alert whenever an S3 bucket is created or deleted). Data at rest was protected using a KMS symmetric customer managed key linked to a DynamoDB table, with user-level access controls defined on the table.<p></p>
