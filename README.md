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
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Lab Information

<p align="center">
<img src="https://imgur.com/E8IGcV1.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Network Diagram</b>
<br/>

- Domain Name: EdLabs.local
- Network : 192.168.10.0/24
 
### Lab Hosts

- Ubuntu 22.04 LTS
  - Splunk Enterprise
- Windows 2016 Domain Controller  
  - Default Domain Controllers Policy
  - Default Domain Policy
  - Sysmon  
  - Splunk Universal Forwarder (Forwards Sysmon)
- Windows 10 Workstation
  - Simulates employee workstation
  - Sysmon  
  - Splunk Universal Forwarder (Forwards Sysmon)  

- Checking network connectivity on hosts
<p align="center">
<img src="https://imgur.com/E8IGcV1.png" height="40%" width="40%" alt="Device Specification"/>
<br/>

- Generate traffic
<p align="center">
<img src="https://imgur.com/E8IGcV1.png" height="40%" width="40%" alt="Device Specification"/>
<br/>

- SIEM's log ingestion and analysis
<p align="center">
<img src="https://imgur.com/E8IGcV1.png" height="40%" width="40%" alt="Device Specification"/>
<br/>

- Wireshark's network capture
<p align="center">
<img src="https://imgur.com/E8IGcV1.png" height="40%" width="40%" alt="Device Specification"/>
<br/>

## Outcome
- Talk about what you achieved, attach screenshots.

- Windows Server 2022 Eval
  - Installed in the virtual machine and promoted to Domain Controller
  - Created domain user accounts
  - Installed and applied custom configuration to Splunk(inputs.conf) and Sysmon (sysmonconfig.xml)

## Acknowledgements
- [Splunk](https://www.splunk.com)
- [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- Splunk Inputs.conf inspired from [MyDFIR](https://github.com/MyDFIR/Active-Directory-Project)
- Sysmon config from [Olaf Hartong](https://github.com/olafhartong/sysmon-modular)
  
