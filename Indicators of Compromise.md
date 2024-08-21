# Indicators of Compromise

## Assignment:
*For this module's assignment, write a short paper that summarizes the indications of a network intrusion and the processes Happy Accident Labs should undertake to detect network intrusions. Use your penetration test activities as a guide. What were some of your activities which could have been detected and how would that have been done? Information from your readings this module, and NIST SP 800-61 section 3.2 should be especially helpful.*

Detecting and responding to network intrusions is vital to maintaining the confidentiality, integrity, and availability of the data your organization is trusted to protect. It is paramount that Happy Accident Labs is capable of identifying and mitigating threats that target its network. Our testing of these capabilities and their findings will be summarized along with recommendations that Happy Accident Labs can take to harden and bolster its network in the future. 
Actions taken during this penetration test would have indicators that would reflect such activity should the environment had been configured appropriately. It was revealed that Happy Accident Labs was unaware of such testing despite knowing such tests were to occur. The including indicators would have revealed such activity:

1. Unusual Network Traffic
   
The tools utilized during the test, such as Aircrack-ng and Metasploit, generate traffic patterns that are distinctive and recognizable by most network monitoring tools. These tools can also monitor for spikes, unusual patterns, or traffic at odd times (Cichonski et al., 2012).

2. Unauthorized Access Attempts
   
During the phase where account access was being evaluated and explored, failed login attempts would have generated alerts in systems like IDS/IPS. Logging and monitoring login attempts would have captured these activities and others, such as successful logins from unusual locations or times (Cichonski et al., 2012).

3. Changes in Network Configuration
   
When the team executed the back door installation of NetCat onto a target host, unauthorized firewall settings were performed. Monitoring the network by auditing configurations and comparing them to the baseline would help identify such activities, including when new devices connect to the network (Cichonski et al., 2012). 

4. Malware and Suspicious Software
   
When the team deployed NetCat on the system, this new software had not been previously authorized. Antivirus and anti-malware tools to detect and alert when unknown or suspicious software is installed (Cichonski et al., 2012).

5. Data Exfiltration
   
Testers could collect data from hosts utilizing the smbclient command and send them to external hosts. Tools that can monitor for large or unusual data transfers can alert and track where and what data has been moved (Cichonski et al., 2012).

Many tools and processes exist that are designed to detect and monitor network intrusions. Recommendations that would bolster the security posture of Happy Accident Lab’s network are included.

1. Establish a Baseline
   
Scan and make note of what the baseline is for Happy Accident Lab’s environment. When activity is detected, it can be compared to this baseline to detect any anomalies or unusual patterns (NIST, 2018).

2. Deploy Network Monitoring Tools
   
Tools such as Snort, which is an IDS/IPS and Splunk, a SIEM, are applications that are designed to monitor networks. They will detect, log, and analyze data and generate alerts based on the customized preference of the organization. This is vital for detection in real-time (Weaver et al., 2014).

3. Conduct Regular Audits and Assessments
   
The network should be regularly audited and assessed as threats and technology are constantly evolving. This ensures that the network remains updated and verifies that it is compliant with policies and regulations. Tools such as OpenVAS, used by the penetration team, can be used to conduct vulnerability scanning and periodic penetration tests (Weaver et al., 2014).

4. Develop an Incident Response Plan
   
Happy Accident Labs must be able to respond to an incident in the event one occurs. Having set procedures for staff to follow during the event will allow a more effective and efficient response and resolution. This plan should also be regularly reviewed and updated (Boyle & Panko, 2021). 

5. Implement Patch Management
   
It is critical that systems remain updated to their latest versions. This prevents known vulnerabilities in those systems from being exploited. Patches provide the necessary updates when new vulnerabilities are discovered and regularly performing patching ensures that systems are protected (Solomon & Oriyano, 2024).

Detecting and responding to network intrusions is vital to maintaining the confidentiality, integrity, and availability of the data your organization is trusted to protect. It is important that Happy Accident Labs is capable of identifying and mitigating threats that target its network. By leveraging insights from the test and implementing the recommendations proposed, Happy Accident Labs can enhance its ability to detect and respond to network intrusions, ensuring the security of its network. 

References:

Solomon, M. and Oriyano, S., (2024). Ethical Hacking: Techniques, Tools, and Countermeasures, 4th Edition. Jones & Bartlett Learning. 

Boyle, R., and Panko, R., (2021). Corporate Computer Security, 5th Edition. Pearson. 

Weaver, R., Weaver, D. and Farwood, D. (2014). Guide to Network Defense and Countermeasures 3rd Edition. Course Technology, Cengage Learning.

Framework for Improving Critical Infrastructure Cybersecurity, (2018, April 16). NIST. Accessed from https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.04162018.pdf. 

Cichonski, P., Millar, T., Grance, T., & Scarfone, K. (2012, August 6). Computer Security Incident Handling Guide. NIST. https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf