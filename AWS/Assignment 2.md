# Application Load Balancer

## Objective
Deploy two EC2 instances behind an ALB. The ALB must handle all incoming traffic. EC2 instances should not be accessible directly from the internet.

## Task 1: Two EC2 Instances 
Launch two EC2 instances in the same VPC

VPC creation:
<img width="2792" height="800" alt="image" src="https://github.com/user-attachments/assets/0f295f80-32c8-4dd3-848c-516af1fde83e" />

## Task 2: Set up the ALB
Add HTTP (port 80) listener & Create a Target Group

<img width="1978" height="478" alt="image" src="https://github.com/user-attachments/assets/11afe218-e3a1-498b-bfb4-5becaf8624d4" />

Configure a health check on the root path /

<img width="2708" height="674" alt="image" src="https://github.com/user-attachments/assets/5de94929-ade0-4d94-8f9a-e7ea44b575fc" />

## Task 3: Security groups
ALB SG: allow HTTP from anywhere

<img width="2844" height="1010" alt="image" src="https://github.com/user-attachments/assets/6dc29fd1-e96f-41da-8ae7-8c11660c3b6e" />


EC2 SG: allow HTTP only from the ALB SG

<img width="3296" height="1458" alt="image" src="https://github.com/user-attachments/assets/ae0357c1-daf2-455f-9b63-4adffaa882bc" />
