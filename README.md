# Tech Solutions Inc.

---

## Scenario / Objective

### Business Scenario: Tech Solutions Inc.

**Company Overview:**
Tech Solutions Inc. is a growing IT consulting firm that provides network solutions and cybersecurity services to small and medium-sized businesses. The company has recently moved into a new office building and needs to set up a robust and secure network infrastructure to support its operations. The office layout includes the following departments:

1. **Administration**
2. **Sales and Marketing**
3. **Technical Support**
4. **Research and Development (R&D)**
5. **Finance**
6. **Human Resources (HR)**

**Network Requirements:**

1. **Network Layout:**
    - The network should include separate VLANs for each department to enhance security and manageability.
    - The main office network will consist of three floors, each housing different departments.
2. **IP Addressing:**
    - Implement a suitable IP addressing scheme using private IP addresses (e.g., 192.168.X.0/24).
    - Each department (VLAN) will have its own subnet.
3. **Routing:**
    - Use a core router to handle inter-VLAN routing.
    - Implement dynamic routing protocols (e.g., OSPF) to ensure efficient routing between different subnets.
4. **Switching:**
    - Use Layer 2 switches to handle intra-VLAN traffic.
    - Implement trunking between switches to support VLANs across multiple switches.
5. **Wireless Network:**
    - Set up a wireless network with access points for guest access and employee mobility.
    - Configure a separate SSID for guests with limited access to the network.
6. **Security:**
    - Implement Access Control Lists (ACLs) on the router to restrict unauthorized access between VLANs.
    - Use port security features on switches to prevent unauthorized devices from connecting to the network.
    - Configure a firewall to protect the network from external threats.
7. **Internet Access:**
    - Configure Network Address Translation (NAT) on the router to enable internet access for all internal devices.
    - Set up a proxy server to monitor and control internet usage.
8. **Servers:**
    - Install and configure essential servers, including a DHCP server, DNS server, and a file server.
    - Ensure redundancy and backup solutions for critical data.
9. **VoIP:**
    - Implement a VoIP system to handle internal and external communication needs.
    - Ensure Quality of Service (QoS) to prioritize VoIP traffic.
10. **Monitoring and Management:**
    - Set up network monitoring tools to track performance and detect issues.
    - Implement a centralized management system to manage devices and configurations.

### Detailed Network Design:

**First Floor (Administration and Sales/Marketing):**

- VLAN 20: Administration (192.168.20.0/24)
- VLAN 30: Sales and Marketing (192.168.30.0/24)

**Second Floor (Technical Support and R&D):**

- VLAN 40: Technical Support (192.168.40.0/24)
- VLAN 50: R&D (192.168.50.0/24)

**Third Floor (Finance and HR):**

- VLAN 60: Finance (192.168.60.0/24)
- VLAN 70: HR (192.168.70.0/24)

**Guest Wi-Fi:**

- VLAN 80: Guest Wi-Fi (192.168.80.0/24)

**Equipment:**

- **Core Router**: Cisco ISR Router
- **Layer 2 Switches**: Cisco 2960 Series Switches
- **Wireless Access Points**: Cisco Aironet
- **Servers**: DHCP, DNS, File Server, Proxy Server
- **Firewall**: Cisco ASA

### Key Objectives:

- Design a scalable and secure network infrastructure.
- Ensure seamless connectivity and communication across all departments.
- Implement robust security measures to protect sensitive company data.
- Provide reliable and controlled internet access.
- Enable efficient network management and monitoring.


## Skills Learned

---

- **Network Design and Planning**:
    - **Device Placement**: Strategically placing network devices.
    - **VLAN Configuration**: Creating and organizing VLANs based on departmental needs.
- **Network Configuration**:
    - **Hostname Configuration**: Setting appropriate hostnames for routers and switches.
    - **DNS Setup**: Configuring DNS on a server and verifying connectivity with ping tests.
- **Documentation and Visualization**:
    - **Color Labeling**: Using visual aids like color labeling to identify departments and floor assignments.
    - **Floor Planning**: Specifying and organizing devices based on physical floor locations.
- **VLAN Management**:
    - **VLAN Creation and Naming**: Setting up VLANs and naming them across multiple switches.
    - **Interface Configuration**: Using interface range commands to configure multiple ports efficiently.
- **Advanced Switching Techniques**:
    - **Trunk Links**: Configuring trunk links for VLAN propagation between switches.
    - **Voice VLANs**: Configuring voice VLANs for all departments.
- **Routing and Inter-VLAN Communication**:
    - **ROAS (Router-on-a-Stick)**: Setting up ROAS for inter-VLAN routing.
    - **Sub-Interface Configuration**: Configuring sub-interfaces on routers for VLANs.
- **DNS Configuration**:
    - **DNS Server Setup**: Configuring the DNS server's IP address, gateway, and DNS settings.
    - **DNS Records**: Creating DNS records and integrating DNS services with the router.
- **DHCP Configuration**:
    - **DHCP Pools**: Setting up DHCP pools for various VLANs.
    - **Helper Address**: Configuring the router's DHCP helper address to relay requests to the DHCP server.
- **IP Address Management**:
    - **Subnetting**: Utilizing subnetting to organize IP address allocation.
    - **Address Assignment**: Ensuring correct IP address assignments for each workstation's VLAN.
- **Network Troubleshooting**:
    - **Ping Tests**: Verifying connectivity and DNS resolution using ping tests.
    - **DHCP Verification**: Checking DHCP address allocation and ensuring clients receive correct configurations.

## Tools Used

---

- **Devices**:
    - **Routers**: Configuring routers with appropriate hostnames and IP addresses.
    - **Switches**: Setting up switches with VLANs and trunk links.
    - **DNS/DHCP Server**: Configuring DNS and DHCP services.
- **VLAN Configuration**:
    - **VLAN Commands**: Creating and naming VLANs on switches.
    - **Interface Range Command**: Applying configurations to multiple interfaces simultaneously.
    - **Trunk Links**: Configuring trunk links for VLAN propagation between switches.
    - **Voice VLAN**: Setting up voice VLANs for specific departments.
- **Routing**:
    - **Router-on-a-Stick (ROAS)**: Configuring sub-interfaces for inter-VLAN routing on routers.
    - **Sub-Interface Configuration**: Setting up sub-interfaces on routers.
- **DNS Configuration**:
    - **DNS Server Setup**: Assigning IP addresses to the DNS server and creating DNS records.
    - **DNS Commands**: Using commands like `ip domain-lookup` and `ip name-server` to configure DNS on routers.
- **DHCP Configuration**:
    - **DHCP Pools**: Creating DHCP pools for different VLANs.
    - **DHCP Helper Address**: Configuring the router with `ip helper-address` to forward DHCP requests.
- **Testing and Verification**:
    - **Ping Tests**: Verifying connectivity with ping tests.
    - **Interface Configuration**: Configuring and verifying interfaces on switches and routers.
- **Color Labeling**:
    - **Visual Aids**: Using color labels to identify departments and floor assignments for better organization.

## Steps

---

![Tech1](https://github.com/Daklan85/Tech-Solutions-Company/blob/main/screenshots/tech1.png)

1. Placed all my devices and made a list of my VLANs. Configured routers and switches with the appropriate hostnames.

![Tech2](https://github.com/Daklan85/Tech-Solutions-Company/blob/main/screenshots/tech2.png)

2. Made my initial connections and set up DNS on the server. Pinged the domain name to ensure it is connected.

![Tech3](https://github.com/Daklan85/Tech-Solutions-Company/blob/main/screenshots/tech3.png)

3. Color-labeled my departments and specified which floor each access switch is located on. Made my connections to my workstations on floor 1, which I will configure first.

### VLANS

---

![Tech4](https://github.com/Daklan85/Tech-Solutions-Company/blob/main/screenshots/tech4.png)

1. Clicked on SW2, created my VLANs, and named them. Repeated this on switches SW1, SW3, and SW4.

![Tech5](https://github.com/Daklan85/Tech-Solutions-Company/blob/main/screenshots/tech5.png)

2. Used the interface range command to select multiple interfaces for my Administration department, created descriptions, and configured access to the VLAN and voice VLAN. Continued this for the rest of floor 1, which includes Sales and Marketing. Then, connected my interfaces to workstations on floors 2 and 3, repeating the steps for the appropriate VLANs as shown in the screenshot above.
3. On the connected links between my access layer switches and my distribution layer switch, configured a trunk link with “switchport mode trunk” on both sides of the link.

![Tech6](https://github.com/Daklan85/Tech-Solutions-Company/blob/main/screenshots/tech6.png)

4. Used ROAS for the inter-VLAN routing option. Configured the connection between my distribution layer switch and my router to be a trunk. Then, went to R1 to configure the sub-interfaces for inter-VLAN routing.

### DNS

---

1. Configured the DNS server. Clicked on my DNS/DHCP server, went to the config tab, clicked on the FastEthernet0 interface, and assigned it the address 192.168.2.2/24. Under the global settings in the config tab, set the default gateway to 192.168.2.1 and the DNS server to 192.168.2.2. Under the Services tab, created a DNS record for 192.168.2.2 and named it www.techsol.com. Next, went to my router R1, and in global config, typed the commands “ip domain-lookup” and “ip name-server 192.168.2.2”. This allows my router to use DNS services and point to my external server.

### DHCP

---

![Tech7](https://github.com/Daklan85/Tech-Solutions-Company/blob/main/screenshots/tech7.png)

1. Clicked on DHCP under the Services tab and configured DHCP pools for all my VLANs. Set the default serverPool max users to 0 so that it does not assign addresses. Input my DNS server and the default gateway from my router on the interface facing the clients. Each sub-interface has a default address reflecting our IP addressing for each department outlined in the objectives at the beginning of the lab. Assigned a start address of x.x.x.10 and allowed 100 max users for each. Each has a /24 mask. Then, navigated to my router and on each router sub-interface, typed the command “ip helper-address 192.168.2.2” to tell the router where to forward the clients' DHCP discover broadcasts. After this, went to each workstation, enabled DHCP, and populated the correct addresses per each workstation’s VLAN.
