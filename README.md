## Objective

In this Detection Lab project was designed to create a controlled setting for simulating and identifying cyber attacks. Its main objective was to process and analyze logs using a Security Information and Event Management (SIEM) system, generating test data to replicate real-world attack situations. This practical experience aimed to enhance knowledge of network security, attack patterns, and defensive measures.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Lab Information

- Domain Name: EdLabs.local
- Network : 192.168.10.0/24
 
### Lab Hosts

- Windows 2016 Domain Controller
  - Default Server Configuration GPO  
  - Default Windows Auditing policy GPO
  - Sysmon  
  - Splunk Universal Forwarder (Forwards Sysmony)
- Windows 10 Workstation
  - Simulates employee workstation
  - Sysmon  
  - Splunk Universal Forwarder (Forwards Sysmon & osquery)  
- Ubuntu 22.04 LTS
  - Splunk Enterprise

## Outcome

<p align="center">
<img src="https://imgur.com/E8IGcV1.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Network Diagram</b>
<br/>

## Acknowledgements
- [Splunk](https://www.splunk.com)
  
