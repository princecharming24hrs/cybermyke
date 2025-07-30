## Catnork – Designing a Secure Internal Network for Improved Operational Efficiency 

### **Business Focus -**
Network Design & Security
### **End nodes or Hardware components required-** 
- Cisco Router 2811
- CAT 6 cables
- 2 Cisco Switches for HR Dept & IT Dept
- 1 DNS Server 
- 1 DHCP Server
- 1 Web Server
- Laptops and computers for the staff 


### SETTING UP THE NETWORK INFRASTRUCTURE
### ** Network Connection** 
- Position all hardware components appropriately consideration safety and high availability and functionality 
- Servers in designated server room
- Switches in the appropriated position for each office / department that will enhance ease of cabling and connection for laptop and computers for staff
- run network connection to all hardware components

### ** Network Configuration** 
Static IP Addresses will be assigned to all devices as follows 

- CISCO ROUTER 
- DHCP SERVER 
- DNS SERVER 
- WEB SERVER
of course network switches don't need ip addresses

THE ROUTER is going to be the connecting device between the switches connecting different section or segment of the infrastructure serving each departments (offices) 
See the diagram below 

So the cisco router  will have 2 LAN ports to link the 2 switches LAN1 & LAN2 with the network configuration below 

| Device | LAN 1 |  LAN 2
| ----- | --- |---|
| | | |
| IP ADDRESS | 192.168.1.1 | 255.255.255.0 
| SUBNET   |  255.255.255.0  | 255.255.255.0
| GATEWAY  |  192.168.1.1  | 192.168.2.1
| DHCP  |  192.168.2.2  | 192.168.2.2
| DNS  |  192.168.2.3  | 192.168.2.3

	


- description - SITUATION
  A law firm wanted to resolve slow internet service and manage slow service for all its staff

- EXPERIENCE
  All the staff were experiencing slow internet service, their computers were having issues with connection to the office network, they also needed to have a setup where some departments can share documents and printer among them, they also wanted their web server to have some level of limitation on who can work on it 

- APPROACH
  Step 1 Setup the Router with different ip routers for different departments 
  step 2 setup a DHCP server that will access ip addresses and also setup different ip segments for different departments
  setp 3 setup a web server  
  setup access list for web server 

- TACTICS
- 

- Links 
- 

### Project 2
- Description
- Links 
- 


Specialization: Network Design & Security Business Focus: Tech Infrastructure for High-Growth Startups
Tool: Packet Trace
