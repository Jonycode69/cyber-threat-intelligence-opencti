#OpenCTI Deployment:
OpenCTI was deployed in a docker environment on Kali Linux.
Docker compose was used to define and manage the OpenCTI services. 
YAML configurations were used to specify services, images, environment variables, credentials, and connector configurations.

OTX Integration:
The AlienVault OTX connector was configured to retrieve community threat intelligence and indicators and feed them into the OpenCTI.
The connector was validated through Docker logs showing OTX pulses being processed and bundled before being sent into the OpenCTI processing pipeline.

Example workflow:
AlienVault OTX —> OTX connector —-> OpenCTI processing pipeline —-> Threat intelligence objects —-> Actors/ Malware/ Infrastructure/ Indicators/ Relationships.

##Threat Landscape Analysis
The assessment focused on threats relevant to telecommunications, including:
- State-sponsored cyber espionage
- Exploitation of internet-facing systems
- Credential theft
- Lateral movement
- Living-off-the-land techniques
- Ransomware
- Phishing and Business Email Compromise
- DDoS attacks
- Abuse of legitimate cloud services for Command and Control
Threat actors investigated included:
- GALLIUM
- APT41
- UNC6619
- Funnull
- SloppyLemming
- Salt Typhoon
##MITRE ATT&CK Analysis:
MITRE ATT&CK was used to identify the specific techniques associated with threat actors.
Examples included:
- Exploitation of Public-Facing Application
- Valid Accounts
- Remote Services
- Credential Dumping
- Network Discovery
- Command and Scripting Interpreter
- Phishing
- Data Exfiltration
MITRE ATT&CK provided the technical detail needed to understand how attackers performed different stages of an intrusion.
##Cyber Kill Chain Analysis:
The Cyber Kill Chain was used to understand the broader progression of an attack.
Reconnaissance —> Weaponization —-> Delivery —-> Exploitation —--> Installation —-> Command and Control (C2) —-> Actions on objectives
MITRE ATT&CK and the Cyber Kill Chain were used together rather than as competing frameworks.
The Kill Chain provided the high-level attack progression, while MITRE ATT&CK provided the specific attacker techniques used within those stages.
##Diamond Model:
Selected incidents were analyzed using the four components of the Diamond Model:
Adversary —-> Capability —-> Infrastructure —--> Victim
This helped establish relationships between:
- Who conducted the activity
- What capabilities/tools were used
- What infrastructure was involved
- Who was targeted
##Key Findings:
The assessment identified several recurring patterns in telecommunications attacks:
- Internet-facing infrastructure is a major attack surface.
- Attackers can exploit vulnerabilities in public-facing applications, VPNs, management systems, and network infrastructure.
- Legitimate administrative tools can be abused.
- Attackers may use tools such as SSH, RDP, PsExec, PowerShell, or legitimate cloud services to blend malicious activity with normal administration.
- Credential compromise enables lateral movement.
- Stolen credentials can allow attackers to access additional internal systems without necessarily deploying obvious malware.
- Telecommunications organizations are valuable espionage targets.
- Telecom infrastructure can provide access to subscriber information, communications data, call records, and network infrastructure.
- Behavior-based detection is therefore critical.
- Security teams cannot rely exclusively on malware signatures. Authentication logs, unusual remote access, lateral connections, privilege changes, and abnormal administrative activity must also be monitored.


##Security Recommendations:
Based on the assessment, CYV should prioritize:
- MFA for remote and privileged access
- Rapid patching of internet-facing systems
- Network segmentation
- Centralized logging and SIEM monitoring
- Monitoring of SSH, RDP, and other remote services
- Privileged account management
- Detection of abnormal authentication and lateral movement
- Endpoint detection and response
- Regular threat-intelligence enrichment
- Incident response and containment procedures
##Skills Demonstrated:
This project demonstrates practical experience with:
- Cyber Threat Intelligence
- OpenCTI
- AlienVault OTX
- Docker and Docker Compose
- YAML configuration
- MITRE ATT&CK
- Cyber Kill Chain
- Diamond Model
- Threat Actor Analysis
- Malware and Tool Analysis
- SOC/SIEM Concepts
- Incident Response
- Threat Landscape Research
- Cybersecurity Risk Assessment
##Conclusion:
This project demonstrated how threat intelligence can be collected, enriched, structured, and analyzed to understand threats against a telecommunications organization.
The key lesson was that effective CTI goes beyond identifying individual malware. It involves connecting adversaries, capabilities, infrastructure, victims, indicators, and attack techniques to produce intelligence that can support detection, investigation, and defensive decision-making.
