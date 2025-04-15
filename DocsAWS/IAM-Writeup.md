# AWS Security: Idenity and Access Managment

**Overview**: 

![image.png](40fd45f7-6325-4edd-8b3f-6fe5d29adb6e.png)

---

### Completed Tasks

- Set up and overview of the project
- Create an IAM user from the console
- Create IAM users from the CLI
- Create IAM groups and add users to the groups
- Implementing IAM policies
- Create and upload to an S3 bucket
- Create an IAM role for an AWS service
- Use IAM roles to grant AWS cross-account access
- Use IAM roles to grant AWS cross-account access with external ID
- Revoke an IAM role
- Setting permissions boundary
- Test and Debug IAM policies using the IAM policy simulator

---

## Project Flow

1. Created an IAM user from console with admin privileges:

![image.png](image.png)

1. Assigned admin permissons to the IAM user account:

![image.png](image%201.png)

1. Configured the AWS CLI on local host CMD & Created sample users from the CLI:

![image.png](image%202.png)

1. Created IAM group  and added users :

![image.png](image%203.png)

~ Granted read/write access to a S3 bucket: 

![image.png](image%204.png)

*Note: Users in an IAM group inherits permissons of the group by default.*

1. Implemented IAM policies(Customer Managed Policy)

~  **Scope**: All AWS resources x **Actions**: Reader rights for IAM components **Group**: CloudSecurityTeam

![image.png](image%205.png)

1. Created and uploaded to an S3 bucket 

~ Note: S3 stores data as objects within buckets. An *object* is a file and any metadata that describes the file. A *bucket* is a container for objects.

![image.png](image%206.png)

1. Created an IAM role for an AWS service [EC2 → S3 ]

![image.png](image%207.png)

1. Used IAM roles to grant AWS cross-account access 

~ Created an IAM role for the Audit team with read only permissons. Confirmed read only acces by attempting to upload to the S3 bucket & creating an EC2 instance. 

![image.png](image%208.png)

![image.png](image%209.png)

1. Used IAM roles to grant AWS cross-acount access with external ID

~ **Note:** Use the SET command to set the security credntials(access key, secret key, and session token) for WIN users and EXPORT for Mac users.

![image.png](image%2010.png)

1. Revoked an IAM role 

~ Enforced revoke action on active sessions. 

![image.png](image%2011.png)

~ Ouput from external Audit acct 

![image.png](image%2012.png)

1. Set permissions boundary 

~ Assigned policy for an IAM user account to prevent the user from modifying permissons. 

![image.png](image%2013.png)

~ Output from IAM user acct with permisson bounday policy assinged

![image.png](image%2014.png)

1. Tested and Debug IAM policies using the IAM policy simulator

![image.png](image%2015.png)

![image.png](image%2016.png)