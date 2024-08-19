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

## Tools Used
   - Kali Linux: The primary operating system used for penetration testing.
   - Netcat (nc): A simple networking tool used to create a backdoor on the target machine.
   - Meterpreter: A payload within Metasploit for interacting with a compromised system.

## Screenshots
Screenshots were taken throughout the process to document access, command execution, and configuration changes.

