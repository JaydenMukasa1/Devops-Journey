# VPC & Networking

# Objective
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
<img width="1429" height="535" alt="Screenshot 2026-03-22 at 15 32 05" src="https://github.com/user-attachments/assets/a4db4802-f526-48b0-867c-655ba71c1e40" />

# 4. EC2 Instances

Public EC2: launch in public subnet with public IP
<img width="2710" height="1332" alt="image" src="https://github.com/user-attachments/assets/566eb981-c31d-4b16-b891-932aa9324ad4" />


Private EC2: launch in private subnet without public IP
<img width="2780" height="1282" alt="image" src="https://github.com/user-attachments/assets/3d2e295f-b6e2-472d-8993-8ef63587c1b6" />


# 5. Security

Public EC2 SG: allow SSH/HTTP only from your IP
<img width="1416" height="262" alt="PUBLIC SECURITY" src="https://github.com/user-attachments/assets/2be08a12-96c1-464f-84be-126cfa55b050" />


Private EC2 SG: allow only internal access (e.g. from public EC2 or Bastion host)
<img width="2774" height="754" alt="image" src="https://github.com/user-attachments/assets/8f36f588-acca-4db7-be99-b484125d6313" />



