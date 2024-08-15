## Description

This week we will be returning to the scanning and enumeration we did in module 4. This time rather than scrolling through the results in a terminal window (or GUI) we will be capturing the output of commands you enter in the terminal window (no GUI this week) in a text file.  We will then search that data using tools such as grep, sed, and regular expressions also known as REGEX.

## Assignment Walk-thru:
Command to enumerate host names with nbtscan.
```zsh
nbtscan 10.19.99.5-20
```

Command to enumerate SMB shares with nmap.
```zsh
nmap –-script smb-enum-shares -p 139,445 10.19.99.5-20
```

Command to enumerate users with nmap.
```zsh
nmap --script smb-enum-users -p 445 10.19.99.5-20
```

Output scan data file.
```zsh
nbtscan 10.19.99.5-20 > HAL_scan
```
<img src="https://i.imgur.com/BYQ6Wwe.png"/>

Concatenate enumeration of SMB shares to host name file.

```zsh
nmap –-script smb-enum-shares -p 139,445 10.19.99.5-20 >> HAL_scan
```

Append enumeration of users to scan file.

```zsh
nmap –script smb-enum-users -p 445 10.19.99.5-20 >> HAL_scan
```
<img src="https://i.imgur.com/TUU28HS.png"/>

utilizing sed command, list host names from scan file.
```zsh
sed -n ‘/IP address/, /Starting Nmap/ {/Starting Nmap/!p}’ HAL_scan
```

<img src="https://i.imgur.com/72bZgpU.png"/>

To list file shares from scan document, utilize grep parameters regex file command.
```zsh
grep -A 2 ‘\\\\’ HAL_scan
```

<img src="https://i.imgur.com/3eTRPdd.png"/>

Utilizing sed command, extract usernames from scan document.
```zsh
sed -n ‘/smb-enum-users/, /|_/p’ HAL_scan
```
<img src="https://i.imgur.com/y9TeU65.png"/>

