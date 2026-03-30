# Application Load Balancer

## Objective
Deploy two EC2 instances behind an ALB. The ALB must handle all incoming traffic. EC2 instances should not be accessible directly from the internet.

## Task 1
Launch two EC2 instances in the same VPC

VPC creation:
<img width="2792" height="800" alt="image" src="https://github.com/user-attachments/assets/0f295f80-32c8-4dd3-848c-516af1fde83e" />



## Task 3 Security groups
ALB SG: allow HTTP from anywhere

<img width="3296" height="1530" alt="image" src="https://github.com/user-attachments/assets/98bf7cc9-77d3-4d4b-abfd-3ab951e40a3e" />

EC2 SG: allow HTTP only from the ALB SG

<img width="3290" height="1320" alt="image" src="https://github.com/user-attachments/assets/7bffae4b-a34e-46ab-876d-1e18914d8115" />
