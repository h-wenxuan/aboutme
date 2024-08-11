---
title: 'SingHealth 2018 Cyber Attack'
date: 2024-08-05
permalink: /posts/2024/08/blog-post-1/
tags:
  - Public Sector
  - Security
  - Cyber Attack
---

By: Wenxuan

One of the most significant cyber attacks in Singapore's history occurred in 2018, targeting SingHealth, the largest government healthcare provider in the country. SingHealth manages a vast network of acute hospitals, national specialty centers, community hospitals, and polyclinics, making it a critical component of Singapore's healthcare system (SingHealth, 2024).

**The Attack and Data Breach**

Over an 8-day period from June 27th to July 4th, 2018, the personal data of 1.5 million Singaporeans was illegally accessed and stolen. This included sensitive information such as NRIC numbers, addresses, genders, races, and dates of birth. Among the stolen data were the outpatient prescriptions of then Prime Minister Lee Hsien Loong and several other ministers. However, despite the data being accessed and copied, the records themselves were not tampered with.

The breach went undetected by the Integrated Health Information Systems (IHiS) until July 4th, 2018, when unusual activity was observed in one of SingHealth’s IT databases. Upon discovering the suspicious activity, IHiS acted swiftly to block further unauthorized access and changed all server and database administration passwords. To further protect its systems, SingHealth also imposed a temporary Internet surfing separation on all staff work computers.

**Investigation of Attack**

The Minister for Communication and Information, S. Iswaran, stated that the attack was likely carried out by an "advanced persistent threat (APT) group" (Channel New Asia, 2018). APT groups are highly sophisticated attackers known for conducting prolonged and meticulously planned cyber campaigns aimed at stealing sensitive information or disrupting operations. 

As a response to the attack, a Committee of Inquiry (COI) was established to thoroughly investigate the breach. The COI released its public report on January 10th, 2019, providing a detailed account of how the attack was executed. The report highlighted the vulnerabilities in SingHealth’s systems and outlined the steps taken to mitigate the damage and prevent future attacks. I have summarised the key points from pages 76 to pages 94 below, mentioning about the timeline that hackers took to conduct the attack in detail. 

![Events]({{ site.baseurl }}/images/events.png)

According to the report, while not conclusive, there is some evidence to suggest the initial intrusion was a result of a successful social engineering attack such as phishing (Ministry of Digital Development and Information, 2019). Phishing is when hackers utilises a person’s trust in big reputable companies and pose as banks to lure victims to click on a link or document that triggers the installation of malware on the device. 

**August to December 2017 (step 1)**

There are 3 malicious artifacts that are found on workstation A:
1. Log File: Remnant from known malware which has password-dumping capability and contained plaintext password credentials of user of Workstation A that attacker stole from RAM typically.
2. Publicly Available Hacking Tool: Installed on 1 December by exploiting a zero-day vulnerability on Microsoft Outlook where patch for vulnerability was yet to be installed on Workstation A. Enables attackers to interact with mail exchange servers remotely and serve as a hidden backdoor. 
3. Remote Access Trojan (RAT 1): Allows attackers to access and control workstation and perform functions such as executing shell scripts remotely and uploading and downloading files.

**December 2017 to June 2018 (step 2)**

After attackers established a foothold in Workstation A, they moved laterally around the network compromising a number of endpoints and servers to try to reach his objective, the SCM database in 3 ways:
1. Malware Spread: The attacker proliferated malware across multiple endpoints and servers. Malware includes stealthy and unique variants that are hard to detect.
2. Powershell Commands: Use by attackers to distribute malware to other machines
3. Windows authentication system: Attackers compromised it and obtained administrator and user credentials from domain controllers,  obtaining full control over all Windows-based servers, hosted applications and underlying data, within domain

**26 June 2018**
![Access]({{ site.baseurl }}/images/access.png)
After spreading the malware, the attacker obtained a password for “L.A. account” through either weak password or credentials in a file system and logged into at least two Citrix servers at the SGH data center. After rounds of unsuccessful attempts to log in to the SCM database from the 2 Citrix servers, the hacker succeeded on 26 June 2018 after obtaining credentials of the “A.A account” from Citrix Server 3. This allowed the hacker to make SQL queries to the database.

**26 June to 4 July 2018**

The attacker querying the database from Citrix Server 2 and there were 3 broad types of SQL queries that attacker ran:
Reconnaissance on schema of SCM database: information on database tables and view, store procedures and predefined SQL codes and functions.
Direct queries relating to individuals: direct queries on specific NRIC numbers, especially then Prime Minister Mr Lee Hsien Loong.
Bulk queries on patients in general

At the same time, data was exfiltrated by the attacker via Workstation A to the attacker’s overseas C2 servers. Soon after on 4th July 2018, IHiS detected the activity and put measures in place to contain the damage done.

Although the attacker did attempt to re-enter the SingHealth Network on 18 and 19 July 2018 by phishing email, no further signs of malicious activity were detected thereafter.

**Learning Points**

All in all, there are many factors that lead to the cyber attack. One factor is that the network connection between the SGH Citrix servers and SCM database were allowed and SGH Citrix servers were not adequately secured against unauthorised access. Moreover, there was a lack of monitoring at the SCM database for unusual queries and access. 

Other than this, there are various lessons we as individuals can learn from it to protect ourselves from cyber attacks:
Be mindful of phishing emails, especially those that use urgent or threatening messages to pressure you to click on links. Also before clicking on clicks, we need to check the authenticity of the email address. 
We need to set a strong password without using personal particulars that can be easily obtained such as phone number or name and avoid using common passwords such as ‘Password123’ or ‘qwerty’.

**References**
1. SingHealth(2024). About SingHealth. SingHealth. Retrieve 05 August 2024 from: [https://www.singhealth.com.sg/](https://www.singhealth.com.sg/)
2. Kevin Kwang(2018). SingHealth cyberattack the work of sophisticated, usually state-linked attackers: Iswaran. Channel News Asia. Retrieve 05 August 2024 from: [https://www.channelnewsasia.com/singapore/singhealth-cyberattack-usually-state-linked-attackers-iswaran-801956](https://www.channelnewsasia.com/singapore/singhealth-cyberattack-usually-state-linked-attackers-iswaran-801956)
3. Committee of Inquiry(2019). Public Report of the Committee of Inquiry into the Cyber Attack on Singapore Health Services Private Limited's Patient Database On or Around 17 June 2018. Ministry of Digital Development and Information. Retrieve 05 August 2024 from: [https://file.go.gov.sg/singhealthcoi.pdf](https://file.go.gov.sg/singhealthcoi.pdf)
