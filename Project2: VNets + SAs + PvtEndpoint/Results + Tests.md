# 1) VNet with 2 Subnets:
- Created a VNet "VNet-Project2" in East US, in RG "RG-Project2"
- A "Subnet-Resources" in which a "TestVM-Project2" will reside
- Another "Subnet-PvtEndpoint" for Private Endpoint to Reside in
- (We can put Pvt Endpoint in "Subnet-Resoruces", but Best practice for Pvt Endpoints is Separate Subnets)

# 2) Storage Account with Public Network Access Disabled
- Created a SA "saproject2" in East US
- SA Itself does not reside in a VNet


# 3) Private Endpoint
- Created one upon SA Creation, right under SA's Networking Blade, "PvtEndpointSA-Project"
- Placed In East US (Doesn't have to be in same Region as SA)
- Resides In "Subnet-PvtEndpoint" In East US, takes an IP from that Subnet's Address Space
- (Private Endpoints in a Region can only communicate w VNets in that Region)
- (Pvt Endpoints in East US To Communicate w VNets in Another Region, we need Global VNet Peering)
