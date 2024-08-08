<p align="center">
<img src="https://i.imgur.com/4hzgUaF.jpeg" alt="Azure logo"/>
</p>

<h1>Lab - Building Intuition for DNS</h1>

- Simple Steps and Description:
  
We'll learn about Domain Name System (DNS) which translates website names into IP addresses.

- Create a DNS Record: Make a record that points a name to an IP address.
- Observe DNS Cache: See how computers remember DNS lookups.
- Create a CNAME Record: Make a record that points one name to another name.
  
This lab is designed to help you understand Domain Name System (DNS) configurations and behavior. You'll create and manage DNS records, understand how DNS caching works, and use tools like 'ping' and 'nslookup' to troubleshoot DNS issues. This project builds your skills in DNS management, a critical aspect of network administration.

<h2>Environments and Technologies Used</h2>

- Azure Portal
- Windows Server 2022 VM (Domain Controller)
- Windows 10 VM (Client)
- DNS Management Tools

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

A-Record Exercise
- Create A-Record:
Log into DC-1 and open DNS Manager.
Create a new A-record for mainframe and point it to DC-1's private IP address.
Log into Client-1 and ping mainframe to verify it works.
Local DNS Cache Exercise

- Modify and Flush DNS:
Change the A-record address to 8.8.8.8.
Ping mainframe from Client-1 and observe it still pings the old address.
Use ipconfig /displaydns to observe the local DNS cache.
Use ipconfig /flushdns to clear the cache.
Ping mainframe again to verify it resolves to the new address.
CNAME Record Exercise

- Create CNAME Record:
Create a CNAME record on DC-1 that points search to www.google.com.
On Client-1, ping search and use nslookup to observe the results.
<img src="https://i.imgur.com/ahjHXVr.png" alt="DNS"/>
