## Objective
Create a custom VPC with one public and one private subnet, set up the correct routing for internet access, and deploy EC2 instances across them.

# 1. Create the VPC
<img width="1396" height="394" alt="Screenshot 2026-03-22 at 15 04 49" src="https://github.com/user-attachments/assets/add023a0-eacb-4399-8335-062b80ebe100" />

# 2. Internet Access 

Attach internet gateway
<img width="1425" height="176" alt="Screenshot 2026-03-22 at 15 07 14" src="https://github.com/user-attachments/assets/18835f8e-534a-4ca3-9931-91a30caee1cd" />

Create Elastic IP
<img width="1417" height="523" alt="Screenshot 2026-03-22 at 15 10 40" src="https://github.com/user-attachments/assets/fa2534a1-3bf1-4cfd-8e72-3841e2840424" />

Create NAT Gateway in the public subnet
<img width="1425" height="575" alt="Screenshot 2026-03-22 at 15 23 34" src="https://github.com/user-attachments/assets/e66b7dd0-36ff-41a4-ba7a-fc527fc41c4a" />

# 3. Route Tables

Public route table → default route via IGW
<img width="1408" height="240" alt="Screenshot 2026-03-22 at 15 27 56" src="https://github.com/user-attachments/assets/434c2979-3b53-434d-af54-71fcf4241370" />

Private route table → default route via NAT Gateway



