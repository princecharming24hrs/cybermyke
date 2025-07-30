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
- Identify and position all hardware components appropriately consideration safety and high availability and functionality 
- **Servers** in designated server room
- **Switches** in the appropriated position for each office / department that will enhance ease of cabling and connection for laptop and computers for staff
- Run **cat 6 cable** for the network connection to all hardware components

### ** Network Configuration** 
**Static IP Addresses** will be assigned to the following devices: 

- CISCO ROUTER 
- DHCP SERVER 
- DNS SERVER 
- WEB SERVER  

**Note** Network switches don't need ip addresses

THE ROUTER is going to be the connecting device between the switches connecting different section or segment of the infrastructure serving each departments (offices) 
See the diagram below 

**ASSIGN IP ADDRESS** TO THE OTHER DEVICES ON THE FIRST SECTION OF THE OFFICE with the **192.168.1.0/24** ranges 
thats is with the ip address ranging from **1 to 254** 
that is   
**192.168.1.1 - 192.168.1.254**   
but we are reserving 1 to 9 for fixed ips to be used by servers and any dedicated devices  
so we will use **192.168.1.10 - 192.168.1.254**  
for any devices that will connect to the network  
and   
a subnet of **255.255.255.0 (/24)** 

the **Gateway** device will be the CISCO ROUTER which we will assign **192.168.1.1** and **192.168.2.1**
because internet access passess or routes through it 

**DNS** resolves all devices or hosts on the network to a hostname and an ip address for easy discovery and location 
it will be assign a fixed IP of **192.168.2.3**

**DHCP** that is responsible to assign ip addresses to all hosts or devices on the network  
So the cisco router  will have 2 LAN ports to link the 2 switches LAN1 & LAN2 with the network configuration below 

| Device | LAN 1 |  LAN 2
| ----- | --- |---|
| | | |
| IP ADDRESS | 192.168.1.1 | 255.255.255.0 
| SUBNET   |  255.255.255.0  | 255.255.255.0
| GATEWAY  |  192.168.1.1  | 192.168.2.1
| DHCP  |  192.168.2.2  | 192.168.2.2
| DNS  |  192.168.2.3  | 192.168.2.3


So with the settings above we begin the 

##**ASSIGN IP ADDRESS CONFIGURATION OF ALL THE NETWORK DEVICES**


CISCO ROUTER IP CONFIGURATION

connect to the router 
enter the command line Interface 
and launch terminal
 from the prompt enter the commands below step by step
 
####### $> configure terminal or conf t  
then Press Enter  
$> enable  
$> ip add  
 
 
 Similarly 
 
 
 | Device | IP ADDRESS | GATEWAY | SUBNET | DNS
| ----- | --- |---| ---|
| DHCP SERVER | 192.168.2.2 | 192.168.2.1| 255.255.255.0| 192.168.2.3|  
| DNS SERVER | 192.168.2.3 | 192.168.2.1| 255.255.255.0| 192.168.2.3|  
| WEB SERVER | 192.168.2.4 | 192.168.2.1| 255.255.255.0| 192.168.2.3|  

DHCP SERVER CONFIGURATION


DNS SERVER CONFIGURATION


WEB SERVER CONFIGURATION


