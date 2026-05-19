# Cloud-Security-Implementation

**COMPANY**: Codtech IT Solutions Private Limited

**NAME**:Parth Girish Kulkarni

**INTERN ID**:CTIS3903

**DOMAIN**:Cloud Computing

**DURATION**:16 Weeks

**MENTOR**:NEELA SANTHOSH

**DISCRIPTION**: Project Overview: Cloud Security Implementation (Task 4)  
This project focused on putting strong Identity and Access Management (IAM) strategies into action. We set up secure data storage on AWS and used encryption protocols to ensure data integrity while enforcing the principle of least privilege.  

Step-by-Step Implementation Breakdown  
Step 1: Enforcing Principle of Least Privilege via IAM  
To secure the infrastructure, we established clear access control. We moved away from using administrative credentials and instead assigned limited, task-specific permissions to the user account parthiam.  
Action: We attached the AWS-managed policy AmazonS3ReadOnlyAccess directly to the IAM user.  
Objective: This change limits the user's ability to interact with Amazon S3 to just reading data, which includes listing and downloading objects. It prevents unauthorized write, modify, or delete actions.  
Result Verification: The IAM console configuration screenshot shows that the AmazonS3ReadOnlyAccess and IAMReadOnlyAccess policies are successfully attached. This confirms that the identity has a restricted read-only role.  

Step 2: Configuring Secure Cloud Storage  
We chose an isolated S3 storage bucket named internship-task1-parth-2026 to host project assets within a structured security framework.  
Action: We kept the default secure infrastructure settings unchanged. This way, any changes or destruction of data would require specific elevated authorization.  
Objective: Our goal was to ensure the storage layer acts like a data vault, resisting unauthorized changes or accidental exposure.  

Step 3: Verifying Security Controls through Deletion Testing  
A critical part of any security setup is testing that the restrictions work in real-world situations. We ran a simulation to check if the IAM policies correctly deny unauthorized destructive actions.  
Action: We attempted to delete a 3.4 KB object named images.jpg from the internship-task1-parth-2026 bucket while logged in as the restricted IAM user.  
Objective: This action aimed to trigger an access failure to show that a read-only user cannot compromise data integrity.  

Task Completion and Results Validation  
The attached screenshots demonstrate the successful completion and verification of the cloud security setup:  
1. Proof of Policy Enforcement (IAM Console)  
The IAM dashboard snippet shows that user parthiam has limited access. The presence of AmazonS3ReadOnlyAccess confirms that the technical barriers are in place.  
2. Proof of Data Protection (S3 Error Status)  
The S3 console status screen confirms that the security measures worked during the deletion test.  
Error Triggered: The console generated a critical alert: "Failed to delete objects."  
Root Cause Verification: The error logs for images.jpg show "Access denied."  

Conclusion: The "Access Denied" message was the expected and ideal outcome for a secured cloud asset. It proves that the IAM policy is effectively stopping unauthorized delete requests. This secures cloud storage against data tampering and loss.

OUTPUT



