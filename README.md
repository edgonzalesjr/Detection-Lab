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
<img src="https://imgur.com/VUDviOE.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Network Diagram</b>
<br/>

- Domain Name: Cosmos.local
- Network : 192.168.2.0/24
 
### Lab Hosts

- Ubuntu 22.04 LTS
  - Splunk Enterprise
- Windows 2022 Eval
  - Default Domain Controller Policy
  - Default Active Directory Policy
  - Sysmon 
  - Splunk Universal Forwarder (Forwards Sysmon)
- Windows 10 Eval
  - Simulates employee workstation
  - Sysmon  
  - Splunk Universal Forwarder (Forwards Sysmon)  

- Checking network connectivity on hosts
<p align="center">
<img src="https://imgur.com/HDXm454.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Splunk Server IP Address and status is running</b>
<br/>

<p align="center">
<img src="https://imgur.com/dojFuld.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Splunk Server reachability</b>
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
  - Installed, configured and promoted as Domain Controller
  - Created domain user accounts
  - Installed and applied custom configuration to Splunk (inputs.conf) and Sysmon (sysmonconfig.xml)

- Windows 10 Pro Eval
  - Installed and applied custom configuration to Splunk(inputs.conf) and Sysmon (sysmonconfig.xml)
  - Joined the Domain
  - Domain user account logged-in
  - Install and setup Atomic Red Team
   - Performed Invoke-AtomicTest based on MITRE ATT&CK framework; 
     - Persistence > Create account (T1136.001)
     - Command and scripting interpreter > PowerShell (T1059.001)

- Attack Machine
  - Using Kali Linux, performed brute force attack using crowbar

## Acknowledgements
- [Splunk](https://www.splunk.com)
- [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- Splunk Inputs.conf inspired from [MyDFIR](https://github.com/MyDFIR/Active-Directory-Project)
- Sysmon config from [Olaf Hartong](https://github.com/olafhartong/sysmon-modular)
  
