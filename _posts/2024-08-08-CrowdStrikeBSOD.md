---
title: 'CrowdStrike’s BSOD'
date: 2024-08-08
permalink: /posts/2024/08/CrowdStrike’s-BSOD/
tags:
  - Engineering & Tech
  - Public Sector
  - Security
---

<br/><img src='/aboutme/images/BSOD.jpg' style='width:300px; height:auto;'>


Blue screen of death (BSOD) also known as kernel panic is a well-known issue among Windows users, It can be triggered by various factors such as outdated drivers, corrupt RAM, or malware infections. However, it shocked the world when millions of Windows systems around the world crashed on July 19, leaving airports struggling to function and impacting many critical operations. To understand the cause of this incident, we first need to delve further into the role of the kernel and the software involved. 

<br/><img src='/aboutme/images/kernel.jpg' style='width:300px; height:auto;'>

The Kernel is often referred to as the “heart” of operating systems. Its primary function is to distribute hardware resources such as CPU, RAM to processes in need and to handle process control tasks, including memory management and system calls required by programs.

Moving on, CrowdStrike is a endpoint security vendor, mainly focusing on their cloud-based software product called Falcon. Falcon is designed to prevent and respond to various types of cyberattacks, thereby minimizing cybersecurity risks. When Falcon platform is used on a computer, it is able to analyse connections to and from the internet to determine if there is any malicious behavior or any threats. It is also able to utilise Artificial Intelligence and Machine Learning to analyse vast amounts of data to identify subtle patterns that might indicate malicious activity such as zero-day attacks. This is achieved through the CrowdStrike Falcon sensor, which monitors network traffic and device driver activity. To perform these tasks, Falcon operates within the Windows kernel. So how did this cause the widespread BSOD?

According to CrowdStrike, the widespread BSOD incident was triggered by a specific update (Rapid Response Content update) to the Falcon platform. This update included a new sensor to “enable visibility into possible novel attack techniques that may abuse certain Windows mechanisms” (CrowdStrike, 2024). However, when it was pushed out, a mismatch occurred during this update: the sensor expected 20 input fields but received 21. This discrepancy led the sensor to attempt reading data from unauthorized memory locations, causing a kernel panic and resulting in BSODs for those who had installed the update—whether automatically or manually.

This incident underscores the critical importance of thoroughly testing all updates before deploying them to production environments. Comprehensive testing should include stress testing and rollback testing—ensuring that systems can revert to a stable state in case of failure during an update. Additionally, in an increasingly interconnected world where cloud services are becoming widespread, maintaining hard copies of important information is crucial for emergency preparedness.

**References**
1. CrowdStrike(2024). External Technical Root Cause Analysis – Channel File 291. CrowdStrike. Retrieve 08 August 2024 from: [https://www.crowdstrike.com/wp-content/uploads/2024/08/Channel-File-291-Incident-Root-Cause-Analysis-08.06.2024.pdf](https://www.crowdstrike.com/wp-content/uploads/2024/08/Channel-File-291-Incident-Root-Cause-Analysis-08.06.2024.pdf)
