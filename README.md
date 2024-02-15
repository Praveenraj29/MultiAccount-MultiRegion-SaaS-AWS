# MultiAccount-MultiRegion-SaaS in AWS

## Scenario

2KC, a newly established company, is embarking on a greenfield initiative to structure its cloud infrastructure. With distinct organizational requirements, 2KC has designated development (dev) and quality assurance (qa) accounts to efficiently cater to its diverse needs.

## Part 1: Setting up Account Landing Zone and Implementing SCP using Control Tower

### Step 1: Control Tower Deployment

**Objective:**
Establish the foundation for multi-account management using AWS Control Tower.

**Procedure:**
1. IAM administrator (iamadmin) initiates the creation of AWS Control Tower.
2. Attaches the identity policy "Adminfullaccess" (default AWS managed policy) to iamadmin for administrative privileges.

### Step 2: Organizational Unit (OU) Structure

**Objective:**
Organize accounts within OUs to align with the company's structure.

**Procedure:**
1. Control Tower establishes a default foundational OU named "Security."
2. "Security" OU houses crucial accounts, including an audit and log account, for centralized security management.
3. iamadmin introduces a custom OU, "2KC," under which specific member accounts will be organized.

### Step 3: Member Account Creation

**Objective:**
Create distinct member accounts within the 2KC OU for specific organizational needs (dev and qa).

**Procedure:**
1. Provision two member accounts, "dev" and "qa," within the custom "2KC" OU.
2. These accounts serve as dedicated environments for development and quality assurance purposes.

### Step 4: Root OU Management

**Objective:**
Establish a clear hierarchy by placing the management account at the root level.

**Procedure:**
1. Position the management account at the root level for overseeing and managing the entire account structure.
2. Ensures centralized control and governance across the organization.

### Step 5: SCP Implementation

**Objective:**
Enforce governance and security measures using Service Control Policies (SCPs).

**Procedure:**
1. IAM administrator defines SCPs within AWS Control Tower to regulate service access.
2. SCPs are associated with relevant OUs, such as "2KC," to ensure that policies are applied to specific accounts.

![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/6f47ae6a-fdf8-410f-a44d-95c95f8fd752)
![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/2ca901ba-02c2-431d-9cbb-c12b29031686)
![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/346f911e-d4b5-4d17-a38f-5639aab03ccf)
![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/3d7238bb-3cd7-4867-9c0b-37979c8c858c)
![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/7bdad29b-3c12-416d-a663-3bed898cf949)
![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/ba618aa4-0b51-4944-b9e0-d7f4c9ea7bfa)
![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/e6565535-6186-47e8-a5f0-69f6e1aefa7c)
![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/631794f7-a802-42d9-b06a-89fcbcf7d1cf)
![image](https://github.com/Praveenraj29/MultiAccount-MultiRegion-SaaS-AWS/assets/44286337/f45f27e7-4f83-4627-bbb8-026956f0136b)








