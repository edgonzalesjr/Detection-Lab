## Objective

In this Detection Lab project was designed to create a controlled setting for simulating and identifying cyber attacks. It's main objective was to process and analyze logs using a Security Information and Event Management (SIEM) system, generating test data to replicate real-world attack situations. This practical experience aimed to enhance knowledge of network security, attack patterns, and defensive measures.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Splunk Enterprise SIEM: For log ingestion, analysis and timeline filtering.
- Ubuntu 22.04 LTS: Used to host the Splunk Enterprise SIEM.
- Windows Server 2022 Eval: Serve as an Active Directory.
- Windows 10 Eval: End-user workstation.
- Wireshark: Network analysis tool for capturing and examining network traffic from a .pcap file.
- Atomic Red Team: Telemetry generation tool to create realistic network traffic and attack scenarios.
- Kali Linux: Penetration testing tool to perform RDP attack on a Windows machine.

## Lab Information

<p align="center">
<img src="https://imgur.com/VUDviOE.png" height="50%" width="50%" alt="Device Specification"/>
<br/>
<b>Network Diagram</b>
<br/>

- Domain Name: Cosmos.local
- Network : 192.168.2.0/24
 
### Lab Hosts

- Ubuntu 22.04 LTS
  - Splunk Enterprise Eval
- Windows Server 2022 Eval
  - Default Domain Controller Policy
  - Default Active Directory Policy
  - Sysmon 
  - Splunk Universal Forwarder (Forwards Sysmon logs)
- Windows 10 Eval
  - Simulates employee workstation
  - Sysmon
  - Splunk Universal Forwarder (Forwards Sysmon logs)
  - Wireshark
- Kali Linux
  - Simulates as attacker's machine

## Practical Exercises

<p align="center">
<img src="https://imgur.com/t77IAZA.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Splunk Server IP Address and status is running.</b>
<br/>

<p align="center">
<img src="https://imgur.com/sy3f32C.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Splunk Server reachability.</b>
<br/>

<p align="center">
<img src="https://imgur.com/JXDn4E4.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Windows Active Directory IP Address.</b>
<br/>

<p align="center">
<img src="https://imgur.com/LmgW0Nw.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Windows Active Directory reachability.</b>
<br/>

<p align="center">
<img src="https://imgur.com/XsJS2FY.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Windows 10 workstation's IP Address and reachability.</b>
<br/>

- Generate traffic
<p align="center">
<img src="https://imgur.com/0LxxDQ7.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Attacker's machine in a failed RDP login attempt to Windows 10 workstation.</b>
<br/>

<p align="center">
<img src="https://imgur.com/Q3ixtbn.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Attacker's machine in a successful RDP login attempt to Windows 10 workstation.</b>
<br/>

<p align="center">
<img src="https://imgur.com/d6O9tOF.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Windows 10 workstation simulating the Atomic Red Team technique id T1136.001. Which map back to MITRE ATT&CK framework, Persistence>Create Local Account.</b>
<br/>

<p align="center">
<img src="https://imgur.com/N2m8bdC.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Windows 10 workstation simulating the Atomic Red Team technique id T1059.001. Which map back to MITRE ATT&CK framework, Execution>Command and Scripting Interpreter>Powershell.</b>
<br/>

- SIEM's log ingestion and analysis
<p align="center">
<img src="https://imgur.com/yJS9mWp.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Splunk Event Code 4625. Failed RDP login attempt.</b>
<br/>

<p align="center">
<img src="https://imgur.com/e9gRIKb.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://imgur.com/0VOpWuE.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Splunk Event Code 4624. Successful RDP login attempt.</b>
<br/>

<p align="center">
<img src="https://imgur.com/iNBP8t2.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://imgur.com/xTam4CQ.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://imgur.com/2rxwYU5.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://imgur.com/R7EEJrr.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://imgur.com/2XE3vHA.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://imgur.com/lhVp402.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Splunk on T1136.001. Which map back to MITRE ATT&CK framework, Persistence>Create Local Account.</b>
<br/>

<p align="center">
<img src="https://imgur.com/VZ8TLS3.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://imgur.com/gMMiZfi.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Splunk on T1059.001. Which map back to MITRE ATT&CK framework, Execution>Command and Scripting Interpreter>Powershell.</b>
<br/>

- Wireshark capture of RDP login attempts on Windows 10 workstation
<p align="center">
<img src="https://imgur.com/1wfWwaP.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Imported the captured pcap file of RDP brute force activity to Wireshark.</b>
<br/>

<p align="center">
<img src="https://imgur.com/f3d7yfr.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Analyze connectivity Duration between Client & Host. Noticed the duration tab, it takes 0.2 seconds on each succeeding attempts, which a clear indication of a brute force activity.</b>
<br/>

## Outcome

- Ubuntu 22.04 LTS
  - Installed and configured Splunk Enterprise Eval.
  - Performed basic Splunk search queries.
- Windows Server 2022 Eval
  - Installed, configured and promoted as Domain Controller.
  - Created domain user accounts.
  - Installed and applied custom configuration to Splunk (inputs.conf) and Sysmon (sysmonconfig.xml).
- Windows 10 Eval
  - Installed and applied custom configuration to Splunk(inputs.conf) and Sysmon (sysmonconfig.xml).
  - Joined the Domain.
  - Domain user account logged-in.
  - Installed and run Wireshark to capture attempted RDP login.
  - Install and setup Atomic Red Team.
   - Performed Invoke-AtomicTest based on MITRE ATT&CK framework; 
     - Persistence > Create account (T1136.001)
     - Command and scripting interpreter > PowerShell (T1059.001)
- Kali Linux
  - Performed brute force attack.
- Should have set up safeguards
  - Follow Company's Acceptable Use Policy.
  - Disable any unnecessary services, such as the Remote Desktop feature in this case.
  - Use a long and complex password for Remote Desktop if it is required in your environment.
  - Implement Zero Trust architecture. Endpoints are verified each time they connect to services and resources on the network.
  - As time advances, so do the organization's security requirements. Ensure that the necessary security measures are implemented.

## Acknowledgements

This project combines ideas and methods from various sources, such as the Splunk Inputs.conf by MyDFIR, Sysmon config by Olaf Hartong, and my personal experience. These resources provided the fundamental information and techniques, which were then modified in light of practical uses.
 - [MyDFIR](https://github.com/MyDFIR/Active-Directory-Project)
 - [Olaf Hartong](https://github.com/olafhartong/sysmon-modular)
 - [Splunk Enterprise](https://www.splunk.com/en_us/products/splunk-enterprise.html)
 - [Ubuntu 22.04 LTS](https://ubuntu.com/)
 - [Windows Server 2022 Eval](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022)
 - [Windows 10 Eval](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise)
 - [Kali Linux](https://www.kali.org/)
 - [Atomic Red Team](https://www.atomicredteam.io/)
 - [Wireshark](https://www.wireshark.org/)
 - [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)

## Disclaimer

The sole goals of the projects and activities here are for education and ethical cybersecurity research. All work was conducted in controlled environments, such as paid cloud spaces, private labs, and online cybersecurity education platforms. Online learning and cloud tasks adhered closely to all usage guidelines. Never use these projects for improper or unlawful purposes. It is always prohibited to break into any computer system or network. Any misuse of the provided information or code is not the responsibility of the author or authors. 
