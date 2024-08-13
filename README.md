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
- Windows Server 2022 Eval
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

<p align="center">
<img src="https://imgur.com/GPotYqu.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Windows Active Directory IP Address</b>
<br/>

<p align="center">
<img src="https://imgur.com/dyB5kNl.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Windows Active Directory reachability</b>
<br/>

<p align="center">
<img src="https://imgur.com/XsJS2FY.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Windows workstation's IP Address and reachability</b>
<br/>

- Generate traffic
<p align="center">
<img src="https://imgur.com/66kVQSi.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Attacker's machine failed attempt</b>
<br/>

<p align="center">
<img src="https://imgur.com/sdEiePr.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Attacker's machine success attempt</b>
<br/>

- SIEM's log ingestion and analysis
<p align="center">
<img src="https://imgur.com/yJS9mWp.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Splunk 4625 - Failed attempt</b>
<br/>

<p align="center">
<img src="https://imgur.com/e9gRIKb.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
 <img src="https://imgur.com/Z0jkymB.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Splunk 4624 - Success attempt</b>
<br/>

- Wireshark's network capture
<p align="center">
<img src="https://imgur.com/40okXRH.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Imported the captured pcap file to Wireshark</b>
<br/>

<p align="center">
<img src="https://imgur.com/boxgZA0.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Analyze connectivity Duration between Client & Host. Noticed the duration tab, it takes 0.2 seconds on each succeeding attempts. Indicating a brute force attack.</b>
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

- Follow Company's Acceptable Use Policy.
- Disable services that are not needed, in this case the Remote Desktop feature.
- Use long and complex password for Remote Desktop if it is required in the environment.
- Implement Zero Trust architecture. Endpoints are verified each time when using any resources on the network.

## Acknowledgements
- [Splunk](https://www.splunk.com)
- [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- Splunk Inputs.conf inspired from [MyDFIR](https://github.com/MyDFIR/Active-Directory-Project)
- Sysmon config from [Olaf Hartong](https://github.com/olafhartong/sysmon-modular)
  
