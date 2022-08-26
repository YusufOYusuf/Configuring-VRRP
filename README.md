<h1>Configuring VRRP</h1>


<h2>Description</h2>
In this lab, I learned to configure VRRP (Virtual Router Redundancy Protocol). It is a protocol that increases availability by providing automatic assignment of available IP routers to hosts.
<br />



<h2>Environments Used </h2>

- <b>Ubuntu 20.04.2 LTS</b> 
- <b>PuTTY SSH Client</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar click PuTTY SSH Client and proceed to put in the IP address, port number, click Telnet and then click open: <br/>
<img src="https://i.postimg.cc/4ycmbh3q/Screen-Shot-2022-08-25-at-10-07-07-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the R11 execute the following command:   <br/>
1. configure terminal <br/>
2. int e0/0 <br/>
3. vrrp 20 ip 10.0.0.3 <br/>
<img src="https://i.postimg.cc/MKKGp47g/Screen-Shot-2022-08-25-at-10-10-23-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
  
<br />
Open a new window from PuTTY SSH Client and enter in the IP address, port number, click Telnet and then click open  <br/>
<img src="https://i.postimg.cc/qM8WWM6T/Screen-Shot-2022-08-25-at-10-14-02-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the R12 terminal window execute the following commands  <br/>
1. configure terminal <br/>
2. int e0/0 <br/>
3. vrrp 20 ip 10.0.0.3 <br/>
<img src="https://i.postimg.cc/QVGCCxjD/Screen-Shot-2022-08-25-at-10-20-12-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the R11 and R12 terminal windows you will observe Init->backup and Init->master. This creates a backup for the VRRP.  <br/>
<img src="https://i.postimg.cc/xCNb1ZLK/Screen-Shot-2022-08-25-at-10-22-01-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />








  
  
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
