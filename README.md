# AWS IAM Incident Response Lab

## Project Overview

This project simulates a compromised IAM role scenario in AWS and demonstrates how cloud administrators can investigate and contain unauthorized access.

The objective was to understand IAM Roles, Trust Policies, Role Assumption, CloudTrail auditing, and access revocation.

---

## Architecture

Ram (Admin User)
↓
Assume IAM Role
↓
CompromisedEC2Role
↓
Access AWS Resources
↓
CloudTrail Logs Activity
↓
Security Investigation
↓
Emergency Deny Policy Applied
↓
Access Revoked

---

## Services Used

* AWS IAM
* AWS STS (Assume Role)
* AWS CloudTrail
* Amazon S3
* Amazon EC2

---

## Project Implementation

### 1. Created IAM Role

Created an IAM role named **CompromisedEC2Role** with:

* AmazonS3ReadOnlyAccess
* AmazonEC2ReadOnlyAccess

### 2. Configured Trust Relationship

Updated the trust policy to allow the IAM user to assume the role.

### 3. Assumed the Role

Used AWS role switching to assume the role and simulate a compromised identity.

### 4. Performed Reconnaissance

Accessed S3 and EC2 resources to simulate attacker reconnaissance activity.

### 5. Investigated Activity

Used CloudTrail Event History to verify that role assumption activity was logged and auditable.

### 6. Contained the Incident

Applied an Emergency Deny policy to immediately revoke access and simulate incident containment.

---

## Key Learnings

* IAM Roles and Trust Policies
* Role Assumption using STS
* CloudTrail auditing and investigation
* AWS access control mechanisms
* Security incident response concepts
* Access revocation and containment

---


