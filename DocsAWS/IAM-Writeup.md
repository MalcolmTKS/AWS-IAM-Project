# AWS Security: Idenity and Access Managment

### Overview: 

![image 18](https://github.com/user-attachments/assets/505bf042-71d6-42d4-9c1d-cbba94b236d1)


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
- Test and debug IAM policies using the IAM policy simulator

---

## Project Flow

### 1. Created an IAM user from the console with admin privileges:

![image.png](image.png)

### 2. Assigned admin permissions to the IAM user account:

![image.png](image%201.png)

### 3. Configured the AWS CLI on local host CMD & Created sample users from the CLI:

![image.png](image%202.png)

### 4. Created IAM group  and added users :

![image.png](image%203.png)

~ Granted read/write access to an S3 bucket: 

![image.png](image%204.png)

*Note: Users in an IAM group inherit the group's permissions by default.*

### 5. Implemented IAM policies(Customer Managed Policy)

~  **Scope**: All AWS resources x **Actions**: Reader rights for IAM components **Group**: CloudSecurityTeam

![image.png](image%205.png)

### 6. Created and uploaded to an S3 bucket 

~ Note: S3 stores data as objects within buckets. An *object* is a file and any metadata that describes the file. A *bucket* is a container for objects.

![image.png](image%206.png)

### 7. Created an IAM role for an AWS service [EC2 → S3 ]

![image.png](image%207.png)

### 8. Used IAM roles to grant AWS cross-account access 

I created an IAM role for the Audit team with read-only permissions. I confirmed read-only access by attempting to upload to the S3 bucket and creating an EC2 instance. 

![image.png](image%208.png)

![image.png](image%209.png)

### 9. Used IAM roles to grant AWS cross-account access with external ID

~ **Note:** Use the SET command to set the security credentials (access key, secret key, and session token) for WIN users and EXPORT for Mac users.

![image.png](image%2010.png)

### 10. Revoked an IAM role 

~ Enforced revoke action on active sessions. 

![image.png](image%2011.png)

~ Ouput from external Audit acct 

![image.png](image%2012.png)

### 11. Set permissions boundary 

~ Assigned policy for an IAM user account to prevent the user from modifying permissions. 

![image.png](image%2013.png)

~ Output from IAM user acct with permission boundary policy assigned

![image.png](image%2014.png)

### 12. Tested and debugged IAM policies using the IAM policy simulator

![image.png](image%2015.png)

![image.png](image%2016.png)
