# Description
Attached to this lab is the file 'HAL.cap'.  This file contains a captured WPA handshake of one of the HAL corporate clients.  Utilizing aircrack-ng in your Kali distribution and the wordlist rockyou.txt determine the pre-shared key for the Happy Accident Labs wifi access point.  Include screen shots of your activity as well as the clear text PSK.

### To start the cracking process for the cap file, the following command was entered:
```
aircrack-ng --b F8:32:E4:52:CA:F8 -w /usr/share/wordlists/rockyou.txt ~/Downloads/HAL.cap. 
```
<img src="https://i.imgur.com/KfZ0GWU.png"/> 1

This is a screen capture of the command executing in aircrack-ng.
<img src="https://i.imgur.com/FtVupBA.png"/> 2

This is the successful cracking of the PSK, which is “huskersare#1”.
<img src="https://i.imgur.com/2pMchnV.png"/> 3
