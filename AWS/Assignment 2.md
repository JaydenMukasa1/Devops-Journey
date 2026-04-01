# Application Load Balancer

## Objective
Deploy two EC2 instances behind an ALB. The ALB must handle all incoming traffic. EC2 instances should not be accessible directly from the internet.

## Task 1: Two EC2 Instances 
Launch two EC2 instances in the same VPC

VPC creation:
<img width="2792" height="800" alt="image" src="https://github.com/user-attachments/assets/0f295f80-32c8-4dd3-848c-516af1fde83e" />

## Task 2: Set up the ALB
Create ALB in two public subnets

<img width="3308" height="1322" alt="image" src="https://github.com/user-attachments/assets/049986f1-3e83-4976-91ac-eb3249311753" />

Add HTTP (port 80) listener & Create a Target Group

<img width="1978" height="478" alt="image" src="https://github.com/user-attachments/assets/11afe218-e3a1-498b-bfb4-5becaf8624d4" />

Configure a health check on the root path /

<img width="2708" height="674" alt="image" src="https://github.com/user-attachments/assets/5de94929-ade0-4d94-8f9a-e7ea44b575fc" />

Register both EC2 Instances

<img width="2746" height="734" alt="image" src="https://github.com/user-attachments/assets/a9d681de-c3b5-4368-8644-2df16b4117cd" />

## Task 3: Security groups
ALB SG: allow HTTP from anywhere

<img width="2844" height="1010" alt="image" src="https://github.com/user-attachments/assets/6dc29fd1-e96f-41da-8ae7-8c11660c3b6e" />


EC2 SG: allow HTTP only from the ALB SG

<img width="3296" height="1458" alt="image" src="https://github.com/user-attachments/assets/ae0357c1-daf2-455f-9b63-4adffaa882bc" />

## Task 4: Testing 

Visit the ALB DNS name & Refresh to verify traffic alternates between both instances

<img width="1527" height="670" alt="Screenshot 2026-04-01 at 20 37 05" src="https://github.com/user-attachments/assets/49e2c914-b15b-401a-8c55-346a4ea0c3db" />

<img width="1533" height="770" alt="Screenshot 2026-04-01 at 20 37 16" src="https://github.com/user-attachments/assets/4515c81f-5100-4922-ab93-01cb04616792" />

Confirm health checks are healthy

<img width="1411" height="459" alt="Screenshot 2026-04-01 at 20 39 21" src="https://github.com/user-attachments/assets/dc6ab6d1-cf4a-4fe3-8627-05ee199b8a25" />

