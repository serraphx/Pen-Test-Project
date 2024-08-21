# Description

Complete the below actions, answering the questions.  Rather than just pasting the screen dumps as answers find the information you need in the scan results and provide that as answers.

### 1. What is the IP address of the Kali box on the HAL network?

Utilizing the command `ip a`, the IP address is 10.19.99.202.

<img src="https://i.imgur.com/SvAQYJu.png.png"/>

*Conduct a ping sweep of the subnet using nmap. For the IP address range you should use the subnet you are on and the last grouping should be 1-100.*

### 2. What are the results of your scan?

The command for a ping sweep is:

```
nmap -sP 10.19.99.1-100
```

The name of the network is HAL_GW.happyaccidentlabs.com 10.19.99.1
Hosts up (7):
- 10.19.99.1
- 10.19.99.5
- 10.19.99.10
- 10.19.99.12
- 10.19.99.14
- 10.19.99.16
- 10.19.99.18


### 3.	Conduct a full open scan on all of the live hosts you discovered, what have you found?

The command for a full open scan is:

```
nmap –v –sT 10.19.99.1-100
```


1. **10.19.99.1**
   - 53/tcp – open, domain
   - 80/tcp – open, http
   - MAC address – 00:50:56:9D:63:AD (VMware)

2. **10.19.99.5**
   - 22/tcp – open, ssh
   - 139/tcp – open, netbios-ssn
   - 445/tcp – open, Microsoft-ds
   - 9090/tcp – open, zeus-admin
   - MAC address – 00:50:56:90:5C:93 (VMware)

3. **10.19.99.10**
   - 135/tcp – open, msrpc
   - 139/tcp – open, netbios-ssn
   - 445/tcp – open, Microsoft-ds
   - 49152/tcp – open, unknown
   - 49153/tcp – open, unknown
   - 49154/tcp – open, unknown
   - 49155/tcp – open, unknown
   - 49156/tcp – open, unknown
   - 49157/tcp – open, unknown
   - MAC address – 00:55:05:69:DF:40 (VMware)

4. **10.19.99.12**
   - 135/tcp – open, msrpc
   - 139/tcp – open, netbios-ssn
   - 445/tcp – open, Microsoft-ds
   - 49152/tcp – open, unknown
   - 49153/tcp – open, unknown
   - 49154/tcp – open, unknown
   - 49155/tcp – open, unknown
   - 49156/tcp – open, unknown
   - 49157/tcp – open, unknown
   - MAC address – 00:55:05:69:D0:16 (VMware)

5. **10.19.99.14**
   - 135/tcp – open, msrpc
   - 139/tcp – open, netbios-ssn
   - 445/tcp – open, Microsoft-ds
   - 5666/tcp – open, nrpe
   - 49152/tcp – open, unknown
   - 49153/tcp – open, unknown
   - 49154/tcp – open, unknown
   - 49157/tcp – open, unknown
   - 49158/tcp – open, unknown
   - 49159/tcp – open, unknown
   - MAC address – 00:55:05:69:D4:88 (VMware)

6. **10.19.99.16**
   - 135/tcp – open, msrpc
   - 139/tcp – open, netbios-ssn
   - 445/tcp – open, Microsoft-ds
   - 5666/tcp – open, nrpe
   - 49152/tcp – open, unknown
   - 49153/tcp – open, unknown
   - 49154/tcp – open, unknown
   - 49157/tcp – open, unknown
   - 49158/tcp – open, unknown
   - 49159/tcp – open, unknown
   - MAC address – 00:55:05:69:D7:2A (VMware)

7. **10.19.99.18**
   - 135/tcp – open, msrpc
   - 139/tcp – open, netbios-ssn
   - 445/tcp – open, Microsoft-ds
   - 5666/tcp – open, nrpe
   - 49152/tcp – open, unknown
   - 49153/tcp – open, unknown
   - 49154/tcp – open, unknown
   - 49157/tcp – open, unknown
   - 49158/tcp – open, unknown
   - 49159/tcp – open, unknown
   - MAC address – 00:55:05:69:D7:D5 (VMware)
 

### 4a.  Run your previous scan against all discovered hosts again but as a stealth scan.  Are the results the same or different?  Explain.

The command for a stealth scan in nmap is:

```
nmap –sS 10.19.99.1-100
```

The two scans were very similar except in the stealth scan; one of the hosts did not have port 139/TCP open, which is described as the NetBIOS, which was host 10.19.99.12.

### 4b. <span style="color: red;"> Run one additional scan of the types shown in your textbook on pages 141-142 on all the hosts you discovered. You can learn more about these types of nmap scans at https://nmap.org/book/man-port-scanning-techniques.html.  What did you find?

```
nmap –sF 10.19.99.1-100
```

I used the -sF scan. I was able to determine hosts that were up, but was not able to determine open ports. Reading through the nmap user guide, this could be due to the operating system used, as Windows does not follow RFC 793, which would result with all the ports looking closed. This could be useful in understanding what OS the hosts may be using, as Unix systems would be more likely to respond appropriately to this type of scan. 

<span style="color: red;">5. Run an OS detection scan against all the active hosts you discovered, report your findings below.</span>

```
nmap –sS –O 10.19.99.1-100
```

- 10.19.99.1
   - Comau embedded (Comau C4G robot control unit) – 92% certainty, was not able to find 1 open and 1 closed port
- 10.19.99.5
   - Linux 3.x/4.x/5.x, Linux 3.10-4.11, Linux 3.2-4.9, Linux 5.1, Linux kernal 5.1, scan notes unreliability due to being unable to find 1 open and 1 closd port
- 10.19.99.10
   - Windows 7 SP0-SP1/Windows Server 2008 SP1, R2/Windows 8/Windows 8.1 Update 1
- 10.19.99.12 
   - Windows 7 SP0-SP1/Windows Server 2008 SP1, R2/Windows 8/Windows 8.1 Update 1
- 10.19.99.14
   - Windows 7 SP0-SP1/Windows Server 2008 SP1, R2/Windows 8/Windows 8.1 Update 1
- 10.19.99.16
   - Windows 7 SP0-SP1/Windows Server 2008 SP1, R2/Windows 8/Windows 8.1 Update 1
- 10.19.99.18
   - Windows 7 SP0-SP1/Windows Server 2008 SP1, R2/Windows 8/Windows 8.1 Update 1

Of note, this scan was not able to determine the operating system used by each host. Instead, it gave a range of possible operating systems it could be.

### 6. Would you run enumforlinux command against all hosts?  If not why not and which ones would you run it against?

You would run this command against all the hosts that are running Windows, as this does not work with hosts that are running anything not Windows or Samba. For this network, I would run it against 10.19.99.10, 10.19.99.12, 10.19.99.14, 10.19.99.16, and 10.19.99.18.

*Run enum4linux against the applicable hosts.*

```
enum4linux –a 10.19.99.10
enum4linux –a 10.19.99.12
enum4linux –a 10.19.99.14
enum4linux –a 10.19.99.16
enum4linux –a 10.19.99.18
```

### 7. What information did you find from your scans?

The enum4linux was not able to gather information about the users of the hosts, but was able to gather the domain/workgroup of them, which was “WORKGROUP.” 10.19.99.10 also included “..__MSBROWSE__.”, which is labeled as a master browser. Each of the hosts have a HAL-PC-00X, from 1-5 in ascending order of the IP addresses. They have File Server Service, Workstation Service, Domain/Workgroup Name, and Browser Service Elections active.

*Start Legion and click on the host panel on the left.  Enter a scan range which is appropriate for the systems on the HAL network you discovered.  Leave the default options selected.  The scan will begin automatically.*

### 8. Did Legion return any additional information you did not get from nmap or enum4linux?  What?

Yes, host 10.19.99.1 is running nginx for its webserver, and pfsense community edition as a firewall, discovered reviewing the screenshot. 10.19.99.5 is running fedora, which was discovered reviewing the screenshots tab. It is also using OpenSSH 7.5 (protocol 2.0). The netbios is using workgroup:samba.

### 9. Submit a system topology (diagram) of what you currently think the network looks like based on what you scans have shown.  Include IPs, types of operating system, users, shares, open ports and anything else you think valuable for later testing.

<img src="https://i.imgur.com/7NIcD2g.png"/>
