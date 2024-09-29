# Pfsense
Firewall 

## Objective
A firewall is a network component  used to allow or deny network traffic at the edge of the network. pfSense is stateful for every traffic it passes through the pfsense no need to specify return policies and it is free open-source firewall and router software.<br>


![Screenshot 2024-09-30 010400](https://github.com/user-attachments/assets/21cdf5e1-d39c-4a8e-bb52-d122a5712ebb)<br>

### Skills Learned
- Understanding how traffic flows through the LAN and WAN network.
- How can we set different policies for firewalls.
- Knowing about different network protocols.


## Steps

Step 1 - Install pfsense iso from their official website<br>

step 2 - set up the VM for pfsense in VMware.<br>
        - choose the RAM and storage. (2 and 10)<br>
        - set network setting, add two networks one is NAT and another is host-only (because we are running pfsense in VM we should take one network as LAN and another as WAN keep in mind).<br>
        
step 3 - now start the pfsense VM <br>
       - accept all the terms <br>
       - allow the installation <br>
       - set LAN and WAN interface differently notice the MAC address.<br>
       
step 4 - it will load in CLI we will see two interfaces LAN and WAN and their IP address and 8 options below.<br>
       - take note of the LAN IP address, it will be like 192.1678.x.x\24<br>
       - open any of the machines it may be Ubuntu, Kali, or Windows this machine should be connected to a LAN network.
       <br>
       
step 5 - On that vm check the IP address using ifconfig or ipconfig it should be within the subnet (like pfsense LAN IP is 192.168.1.0\24 then ip of vm machine should be 192,168.1.10).<br>
       - see the subnet in IP details it has pfsense IP <br>
       - Now open browser and type the subnet ip it would be like 192.168.1.1 <br>
       - it runs on HTTP processed using the advanced option.<br>
       
step 6 - You will enter the pfsense login page.<br>
       -  The username and password are admin and pfsense.<br>
       - you will see the pf sense dashboard it contain all the information of running vm machine and many options like firewall, interface, service,Vpn.<br>
       
step 7 - on the state table, will find all ips of traffic <br>
       - u can set different rules for WAN and LAN interface<br>
       - now set firewall rules by clicking on firewall and selecting the interface u will see the option like add,delete,modify.<br>
       - now add rules action may be pass, allow, deny<br>
       - choose the IP format v4 or v6<br>
       - choose the protocol TCP UDP ICMP any of them.<br>
       - now set the source it's our VM machine u can choose the single ip or full subnet <br>
       - and set the destination as the firewall itself.<br>
       - and save u will find ur rule displayed <br>
       
  step 8 - u can set protocal TCP and try to ping u will not get <br>
         - use diffent type of protocols and try around it<br>
         
  step 9 - to use multiple ports can use allases>ports<br>
         - u can set the aliases in the destination others>custom option u can set the aliases.<br>
         
  step 10 - for browsing u should set DNS 53 port<br>
          -on the system log u will see which IPs are allowed and denied.<br>
          

  
         
 
