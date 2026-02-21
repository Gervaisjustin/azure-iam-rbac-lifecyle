# azure-iam-rbac-lifecyle
# Azure Entra ID – RBAC & IAM Lifecycle Implementation

## 📌 Project Overview

This project demonstrates the design and implementation of a role-based access control (RBAC) model using Microsoft Azure Entra ID.

The objective was to simulate a real-world enterprise IAM environment including:

- Group-based access control
- Least-privilege enforcement
- Segregation of duties (SoD)
- Secure onboarding and offboarding workflows
- Conditional Access enforcement with MFA

---

## 🏗 Environment

- Microsoft Azure Portal
- Microsoft Entra ID (Free Tier)
- Security Groups
- Enterprise Applications (Non-Gallery Apps)
- Conditional Access Policies

---

## 👥 Role-Based Access Model

Security groups aligned to business functions:

- HR_Users
- Finance_Users
- Engineer_Users
- IAM_Admins

Access to enterprise applications was assigned strictly through group membership.  
Direct user-to-application assignments were intentionally avoided to prevent privilege creep.

---

## 🖥 Enterprise Applications Created

1. Payroll-Portal  
   Assigned: HR_Users, Finance_Users  

2. DevOps-Tool  
   Assigned: Engineer_Users  

3. Admin-Console  
   Assigned: IAM_Admins  

This model enforces least privilege and segregation of duties.

---

## 🔄 User Lifecycle Simulation

### Onboarding Process
1. Created new user in Entra ID.
2. Assigned user to appropriate security group.
3. Application access automatically provisioned via group membership.

### Offboarding Process
1. Blocked user sign-in.
2. Removed user from all security groups.
3. Verified application access revocation.

---

## 🔐 Security Controls Implemented

- Role-Based Access Control (RBAC)
- Group-based assignment model
- Segregation of Duties enforcement
- Conditional Access with MFA
- Legacy authentication blocking

---

## 📊 Access Review & Governance

An access review was conducted to identify:

- Over-privileged accounts
- Dormant users
- Segregation-of-duties conflicts

Risk ratings were assigned and remediation actions documented.

See `/access-review` folder for documentation.

---

## 🎯 IAM Concepts Demonstrated

- Least Privilege
- Role Engineering
- Lifecycle Management
- Access Governance
- Zero Trust Principles
- Privileged Access Segmentation
