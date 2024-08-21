# Risk Analysis

*In this module, you will document those vulnerability findings as well as associated root cause, proof of concept, impact, likelihood, and resultant risk in the penetration test report you are developing. Your findings will appear in at least three, and possibly four, areas in your pentest report. For this module, you will work on numbers two and three.*

   1. *You will summarize the high-risk findings in the executive summary.*
   2. *You will summarize all findings in the list of findings section.*
   3. *You will provide details on all vulnerabilities in the findings detail section.*
   4. *Any amplifying or clarifying information on vulnerabilities should be included in the report appendix.*


### Findings Table

| Vulnerability   | Host(s)                                     | Impact   | Likelihood | Risk     |
| --------------- | ------------------------------------------- | -------- | ---------- | -------- |
| CVE-2017-0143   | 10.19.99.10                                 | Critical | Very High  | Critical |
| CVE-2017-0144   | 10.19.99.10                                 | Critical | Very High  | Critical |
| CVE-2017-0145   | 10.19.99.10                                 | Critical | Very High  | Critical |
| CVE-2017-0146   | 10.19.99.10                                 | Critical | Very High  | Critical |
| CVE-2017-0147   | 10.19.99.10                                 | Critical | Very High  | Critical |
| CVE-2017-0148   | 10.19.99.10                                 | Critical | Very High  | Critical |
| CVE-1999-0519   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | Moderate | High       | High     |
| CVE-2006-3439   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2010-2550   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2010-2551   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2010-2552   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2010-0020   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2010-0021   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2010-0022   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2010-0231   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2009-2526   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2009-2532   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |
| CVE-2009-3103   | 10.19.99.10, 10.19.99.14, 10.19.99.16, 10.19.99.18 | High     | High       | Critical |

### Detailed Findings

#### CVE-2017-0143 (EternalBlue)
  - **Definition**: A remote code execution vulnerability in the SMBv1 protocol in Microsoft Windows.
  - **Root Cause**: Improper handling of specially crafted SMBv1 packets.
  - **Proof of Concept**: Exploited by WannaCry ransomware; [exploit-db.com/exploits/43970](https://www.exploit-db.com/exploits/43970).
  - **Impact**: Critical. Full system compromise.
  - **Likelihood**: Very High. Widely known, and publicly available exploits exist.
  - **Access**: Remote (WAN/LAN), repeatable.
  - **Resultant Risk**: Critical. High impact and high likelihood.
  - **Recommendation**: Disable SMBv1, apply patches (MS17-010).

#### CVE-2017-0144 (EternalBlue)
- **Definition**: A remote code execution vulnerability in the SMBv1 protocol in Microsoft Windows.
- **Root Cause**: Improper handling of specially crafted SMBv1 packets.
- **Proof of Concept**: Exploited by WannaCry ransomware; [exploit-db.com/exploits/43970](https://www.exploit-db.com/exploits/43970).
- **Impact**: Critical. Full system compromise.
- **Likelihood**: Very High. Widely known, and publicly available exploits exist.
- **Access**: Remote (WAN/LAN), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Disable SMBv1, apply patches (MS17-010).

#### CVE-2017-0145 (EternalBlue)
- **Definition**: A remote code execution vulnerability in the SMBv1 protocol in Microsoft Windows.
- **Root Cause**: Improper handling of specially crafted SMBv1 packets.
- **Proof of Concept**: Exploited by WannaCry ransomware; [exploit-db.com/exploits/43970](https://www.exploit-db.com/exploits/43970).
- **Impact**: Critical. Full system compromise.
- **Likelihood**: Very High. Widely known, and publicly available exploits exist.
- **Access**: Remote (WAN/LAN), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Disable SMBv1, apply patches (MS17-010).

#### CVE-2017-0146 (EternalBlue)
- **Definition**: A remote code execution vulnerability in the SMBv1 protocol in Microsoft Windows.
- **Root Cause**: Improper handling of specially crafted SMBv1 packets.
- **Proof of Concept**: Exploited by WannaCry ransomware; [exploit-db.com/exploits/43970](https://www.exploit-db.com/exploits/43970).
- **Impact**: Critical. Full system compromise.
- **Likelihood**: Very High. Widely known, and publicly available exploits exist.
- **Access**: Remote (WAN/LAN), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Disable SMBv1, apply patches (MS17-010).

#### CVE-2017-0147 (EternalBlue)
- **Definition**: A remote code execution vulnerability in the SMBv1 protocol in Microsoft Windows.
- **Root Cause**: Improper handling of specially crafted SMBv1 packets.
- **Proof of Concept**: Exploited by WannaCry ransomware; [exploit-db.com/exploits/43970](https://www.exploit-db.com/exploits/43970).
- **Impact**: Critical. Full system compromise.
- **Likelihood**: Very High. Widely known, and publicly available exploits exist.
- **Access**: Remote (WAN/LAN), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Disable SMBv1, apply patches (MS17-010).

#### CVE-2017-0148 (EternalBlue)
- **Definition**: A remote code execution vulnerability in the SMBv1 protocol in Microsoft Windows.
- **Root Cause**: Improper handling of specially crafted SMBv1 packets.
- **Proof of Concept**: Exploited by WannaCry ransomware; [exploit-db.com/exploits/43970](https://www.exploit-db.com/exploits/43970).
- **Impact**: Critical. Full system compromise.
- **Likelihood**: Very High. Widely known, and publicly available exploits exist.
- **Access**: Remote (WAN/LAN), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Disable SMBv1, apply patches (MS17-010).

#### CVE-1999-0519
- **Definition**: A NETBIOS/SMB share password is the default, null, or missing.
- **Root Cause**: Weak default configurations.
- **Proof of Concept**: Automated scanning tools detect default community strings.
- **Impact**: Moderate. Unauthorized access to SNMP data.
- **Likelihood**: High. Publicly known.
- **Access**: Network, repeatable.
- **Resultant Risk**: High. Moderate impact and high likelihood.
- **Recommendation**: Change default configurations and use strong unique values.

#### CVE-2006-3439
- **Definition**: Remote code execution in Internet Explorer.
- **Root Cause**: Improper handling of objects in memory.
- **Proof of Concept**: Exploited with specially crafted packets to vulnerable Windows systems that trigger a buffer overflow; [exploit-db.com/exploits/16367](https://www.exploit-db.com/exploits/16367).
- **Impact**: High. Execution of arbitrary code.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (via malicious website/email), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Apply security updates (MS06-040), use updated browsers.

#### CVE-2010-2550
- **Definition**: Remote code execution in DirectShow.
- **Root Cause**: Memory corruption.
- **Proof of Concept**: Exploited via specially crafted media files; [exploit-db.com/exploits/16574](https://www.exploit-db.com/exploits/16574).
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (media file delivery), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Apply patches (MS10-046), avoid opening untrusted media files.

#### CVE-2010-2551
- **Definition**: Remote code execution in DirectShow.
- **Root Cause**: Memory corruption.
- **Proof of Concept**: Exploited via media files; [exploit-db.com/exploits/16574](https://www.exploit-db.com/exploits/16574).
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (media file delivery), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Apply patches (MS10-046), avoid untrusted media files.

#### CVE-2010-2552
- **Definition**: Remote code execution in DirectShow.
- **Root Cause**: Memory corruption.
- **Proof of Concept**: Exploited via media files; [exploit-db.com/exploits/16574](https://www.exploit-db.com/exploits/16574).
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (media file delivery), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Apply patches (MS10-046), avoid untrusted media files.

#### CVE-2010-0020
- **Definition**: Remote code execution via AVI files.
- **Root Cause**: Improper handling of AVI files.
- **Proof of Concept**: Delivered via malicious AVI files.
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (file delivery), repeatable.
- **Resultant Risk**: Critical. High risk and high likelihood.
- **Recommendation**: Apply patches (MS10-013), avoid untrusted AVI files.

#### CVE-2010-0021
- **Definition**: Remote code execution in Windows Media Player.
- **Root Cause**: Memory corruption.
- **Proof of Concept**: Delivered via malicious media files.
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (file delivery), repeatable.
- **Resultant Risk**: Critical. High risk and high likelihood.
- **Recommendation**: Apply patches (MS10-013), avoid untrusted media files.

#### CVE-2010-0022
- **Definition**: Remote code execution in Windows Media Player.
- **Root Cause**: Memory corruption.
- **Proof of Concept**: Delivered via malicious media files.
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (file delivery), repeatable.
- **Resultant Risk**: Critical. High risk and high likelihood.
- **Recommendation**: Apply patches (MS10-013), avoid untrusted media files.

#### CVE-2010-0231
- **Definition**: Remote code execution via MIDI files.
- **Root Cause**: Improper handling of MIDI files.
- **Proof of Concept**: Delivered via malicious MIDI files; [exploit-db.com/exploits/15266](https://www.exploit-db.com/exploits/15266).
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (file delivery), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Apply patches (MS10-030), avoid untrusted MIDI files.

#### CVE-2009-2526
- **Definition**: Remote code execution in GDI+.
- **Root Cause**: Improper handling of malformed images.
- **Proof of Concept**: Exploited via specially crafted image files; [exploit-db.com/exploits/40280](https://www.exploit-db.com/exploits/40280).
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (file delivery), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Apply patches (MS09-062), avoid untrusted images.

#### CVE-2009-2532
- **Definition**: Remote code execution in GDI+.
- **Root Cause**: Improper handling of malformed images.
- **Proof of Concept**: Exploited via specially crafted image files; [exploit-db.com/exploits/40280](https://www.exploit-db.com/exploits/40280).
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (file delivery), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Apply patches (MS09-062), avoid untrusted images.

#### CVE-2009-3103
- **Definition**: Remote code execution via crafted web pages.
- **Root Cause**: Improper handling of web content.
- **Proof of Concept**: Delivered via malicious websites; [exploit-db.com/exploits/47456](https://www.exploit-db.com/exploits/47456).
- **Impact**: High. Arbitrary code execution.
- **Likelihood**: High. Well-known and exploited.
- **Access**: Remote (web browser), repeatable.
- **Resultant Risk**: Critical. High impact and high likelihood.
- **Recommendation**: Apply patches (MS09-062), avoid untrusted websites.

#### Improper Vulnerability Detection
- **Root Cause**: Lack of security policies, improper configurations, and environment tools to detect and identify vulnerabilities and respond to them.
- **Impact**: Critical. The inability to detect vulnerabilities may lead to complete system compromise, resulting in data exfiltration and system manipulation.
- **Likelihood**: High. Ease of exploitation of known vulnerabilities of hosts within the network with publicly accessible exploits.
- **Access**: LAN access, repeatable.
- **Resultant Risk**: Critical. Critical impact and high likelihood.

**Detecting and responding to network intrusions** is vital for securing data confidentiality, integrity, and availability. The penetration test at Happy Accident Labs revealed significant flaws in their ability to detect threats, evidenced by the failure to detect simulated intrusions. Key indicators of intrusion activity, including unusual network traffic, unauthorized access attempts, network configuration changes, malware, and data exfiltration, were not detected.

### Key Findings:
- Unusual network traffic generated by tools like Aircrack-ng and Metasploit went undetected.
- Unauthorized access attempts were not flagged following failed login attempts and suspicious logins.
- Network configuration modifications to the firewall and new device connections went unnoticed.
- Unauthorized installations of software like NetCat were missed.
- Data exfiltration of company resources such as business plans was not monitored effectively.

### Recommendations:
1. **Establish a Baseline**: Define normal network activity to identify anomalies.
2. **Deploy Monitoring Tools**: Implement IDS/IPS and SIEM tools for real-time monitoring and alerting.
3. **Conduct Regular Audits**: Perform frequent security audits and vulnerability assessments.
4. **Develop an Incident Response Plan**: Create and regularly update a response plan to handle security incidents effectively.