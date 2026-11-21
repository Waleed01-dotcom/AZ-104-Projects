# Project2: VNets + SAs + PvtEndpoint

<img width="1752" height="897" alt="image" src="https://github.com/user-attachments/assets/1401bd4d-a87e-4cf6-8aba-ada45ef430b3" />

# 1) VNet with 2 Subnets:
- Create one subnet for your resources (such as a VM) and a dedicated second subnet for Private Endpoints


# 2) Storage Account with Public Access Disabled:
- Create a SA, Disable all Public Network Access

# 3) Private Endpoint:
- Deploy a Private Endpoint that connects SA directly to VNet


# 4) Network Security Group (NSG):
- Configure Inbound & Outbound Security Rules, that restrict Network Traffic strictly to what's Explicitly Allowed


# 5) ARM Template:
- Export or write an ARM template to Automate Redeployment of this Entire Environment


# 6) Verification:
- Test Connectivity: Confirm that a VM in VNet "Subnet-Resources" can reach SA's Pvt Endpoint "Subnet-PvtEndpoint", while a VM outside the VNet cannot
- IaC: Practice Redeploying this Setup via ARM Template
