# Information-security-governance-Week-5-
Build an isolated Docker-based simulation. Identify vulnerabilities, weak authentication, segmentation gaps and governance failures. Analyse the simulated findings against the Equifax breach case study. Implement and verify patch-management, monitoring, segmentation, database-security and governance-oversight controls.
Part 1:Setting Up a Simulated Environment

SCREENSHOT SHOWING THE DOCKER ENVIRONMENT SETUP
Figure 1 –Docker-based simulated security governance environment showing the web server, database server, and monitoring server running on the secgov_network 

<img width="1357" height="298" alt="Screenshot 2026-10-07 144653" src="https://github.com/user-attachments/assets/f7d78cf4-13b1-4c9c-9f52-d46385b7bfbf" />

THE VULNERABILITY SCAN REPORT
Figure 2: Vulnerability scan identifying the critical Apache Struts2 S2-045 vulnerability, high-severity MySQL default credentials, and an unknown network-segmentation result caused by a scanner processing error. 
The scan identified one critical vulnerability and one high-severity vulnerability. The network segmentation check returned an unknown result because of a scanner processing error. 
<img width="1358" height="524" alt="Screenshot 2026-10-07 145502" src="https://github.com/user-attachments/assets/d6e6ea3c-e007-4a88-ad0c-d5b64aa9af86" />

THE GOVERNANCE TRACKER DASHBOARD
Figure 3: Governance tracker dashboard showing the simulated organization's policies, controls, risks, incidents, and security metrics. 
<img width="454" height="373" alt="Screenshot 2026-10-07 151459" src="https://github.com/user-attachments/assets/09b83446-7b30-4a5a-a952-aa331529c1e3" />

Relationship to the equifax breach
The simulated environment reflects several key conditions that contributed to the Equifax breach. The web server runs a vulnerable version of Apache Struts affected by CVE-2017-5638 (S2-045), representing an organization failing to remediate a known critical vulnerability. The environment also contains a database with weak/default credentials, demonstrating inadequate access controls. In addition, the web server and database are connected within the same Docker network, simulating insufficient network segmentation that could allow an attacker who compromises the web server to reach sensitive database resources.
The environment also demonstrates governance weaknesses rather than focusing only on technical vulnerabilities. Although governance policies, controls, risks, incidents, and metrics have been defined, the simulated environment shows that controls are not necessarily effective simply because they exist. The unpatched vulnerability and unresolved database security issue represent gaps between security governance requirements and actual implementation, similar to the conditions highlighted in the Equifax case.





Part 2 : Analysing Security Governance Failures

Figure 1: Simulated exploitation of the vulnerable Apache Struts application, demonstrating the potential progression from vulnerability exploitation to database access and simulated customer-data exfiltration. 
<img width="597" height="145" alt="Screenshot 2026-10-07 154442" src="https://github.com/user-attachments/assets/606d454b-8dba-4475-bb8c-c4d6f32e22cf" />

Figure 2: Governance failure analysis identifying weaknesses in patch management, security monitoring, security architecture, and authentication and access control. 
<img width="879" height="141" alt="Screenshot 2026-10-07 155005" src="https://github.com/user-attachments/assets/21d57a08-5117-42fb-8353-7c3f0a83da4a" />


THE COMPARISON REPORT BETWEEN THE SIMULATED ENVIRONMENT AND THE EQUIFAX CASE

cat equifax_comparison.md                                                                                                                                          
# Comparison of Simulated Environment to Equifax Data Breach

## Overview

This report compares the security governance failures identified in the simulated environment with key conditions that contributed to the 2017 Equifax data breach.

## 1. Patch Management Failure

**Equifax:** Equifax failed to properly identify the vulnerable Apache Struts system and ensure that the required security patch was applied.

**Simulated Environment:** The web server contains the Apache Struts S2-045 vulnerability (CVE-2017-5638), which remains unpatched.

**Governance Lesson:** Critical vulnerabilities must be identified, assigned to responsible owners, remediated within defined timeframes, and verified after remediation.

## 2. Security Monitoring Failure

**Equifax:** The breach remained undetected for an extended period. GAO reported that an expired digital certificate prevented a network-monitoring tool from performing its intended detection function.

**Simulated Environment:** The attack simulation demonstrates successful exploitation and simulated data access without real-time security detection.

**Governance Lesson:** Security monitoring controls must be continuously maintained, tested, and monitored to ensure they actually operate as intended.

## 3. Network Segmentation Failure

**Equifax:** Attackers were able to use the compromised portal to communicate with other systems and access sensitive databases, demonstrating the importance of effective segmentation.

**Simulated Environment:** The web server and database are connected through the same Docker network, representing insufficient segmentation in the simulated environment.

**Governance Lesson:** Sensitive systems and databases should be appropriately segmented and access should follow the principle of least privilege.

## 4. Authentication and Access Control Failure

**Equifax:** Attackers discovered credentials that enabled access to additional databases, expanding the scope of the compromise.

**Simulated Environment:** The MySQL database uses default credentials, creating a simulated weakness in authentication and access control.

**Governance Lesson:** Strong authentication, appropriate access restrictions, and secure credential management are essential for protecting sensitive information.

## 5. Policy Implementation and Accountability

**Equifax:** The breach demonstrates that having security processes and policies is not sufficient if controls are not effectively implemented, monitored, and maintained.

**Simulated Environment:** Governance policies and controls have been recorded in the governance tracker, but critical vulnerabilities and risks remain open.

**Governance Lesson:** Governance controls require clear ownership, accountability, evidence of implementation, and regular review.

## 6. Metrics and Measurement

**Equifax:** The incident demonstrates the importance of effective security metrics and oversight for identifying unresolved security weaknesses.

**Simulated Environment:** The governance tracker contains metrics for patch compliance, security monitoring coverage, and high-risk remediation. Their current values remain at 0%, demonstrating that identified security issues have not yet been remediated.

**Governance Lesson:** Security metrics should be actionable and linked to ownership, remediation activities, and management oversight.

## Conclusion

The simulated environment reproduces several governance conditions that are comparable to those associated with the Equifax breach: an unpatched critical vulnerability, weaknesses in monitoring, inadequate segmentation, weak authentication, and gaps between documented governance controls and their effective implementation. The simulation demonstrates that cybersecurity governance is not only about establishing policies but also about ensuring that controls operate effectively and that identified risks are addressed.

The key lesson is that vulnerability management, monitoring, access control, network segmentation, accountability, and measurable security objectives must work together. A weakness in one area can increase the impact of weaknesses in other areas, making effective governance, continuous monitoring, and timely remediation essential for protecting sensitive information.



BRIEF EXPLANATION OF THE LESSON LEARNED
The analysis demonstrates that effective information security governance goes beyond simply creating policies and controls. Organizations must ensure that critical vulnerabilities are identified, assigned to responsible owners, remediated within defined timeframes, and verified. The simulation also highlights the importance of continuous security monitoring, strong authentication and access controls, and appropriate network segmentation to reduce the potential impact of a compromise.
Another key lesson is the importance of accountability and measurable security governance. Security risks and controls need clear ownership, while metrics should be used to identify unresolved weaknesses and drive corrective action. The comparison with the Equifax breach shows that when governance controls are not effectively implemented, monitored, and maintained, known technical weaknesses can develop into significant security incidents.





Part 3: Implementing Security Governance Controls
Figure 1 – Security Governance Control Implementation
 The implementation included applying the Struts2 security patch, implementing network segmentation rules, securing the MySQL configuration, creating a security monitoring script, and establishing governance oversight documentation. These controls directly address the identified weaknesses in patch management, network security, database access control, security monitoring, and governance accountability.
<img width="919" height="451" alt="Screenshot 2026-10-07 163456" src="https://github.com/user-attachments/assets/09ec6b41-678b-4c02-b9cf-598c770f8164" />


 
Figure 2 – Security Governance Control Verification 
<img width="586" height="205" alt="Screenshot 2026-10-07 164512" src="https://github.com/user-attachments/assets/94709b92-e465-45bd-9495-9829edef698a" />

Figure 3 – Post-Implementation Security Verification 
The post-implementation verification included rerunning the simulated attack against the web application. The simulation successfully detected the Struts2 S2-045 vulnerability and proceeded through the simulated database access and data-exfiltration stages. This demonstrates that the simulated vulnerable condition remained observable during verification and highlights the importance of validating the effectiveness of implemented controls rather than relying solely on control implementation status. 
<img width="546" height="147" alt="Screenshot 2026-10-07 170138" src="https://github.com/user-attachments/assets/4002827c-07b7-4da5-9b65-ccb3dedcad5e" />

HOW THE CONTROLS ADDRESS THE GOVERNANCE FAILURES IDENTIFIED IN THE EQUIFAX BREACH
The implemented security governance controls directly address the governance failures identified in the Equifax case study by strengthening patch management, network segmentation, database access control, and security monitoring. The patch management control ensures that critical vulnerabilities such as the simulated Apache Struts2 vulnerability are identified and addressed, reducing the period in which known vulnerabilities remain exploitable. Network segmentation limits unnecessary communication between systems, while improved database security strengthens authentication and access controls around sensitive customer information. Security monitoring also provides ongoing visibility into security conditions so that weaknesses can be identified and addressed more quickly.
The governance oversight control addresses the accountability and management weaknesses associated with the Equifax case by defining responsibilities for management, security teams, system owners, and the governance function. Regular review of risks, control effectiveness, and remediation progress helps ensure that security requirements are not merely documented but are actively monitored and managed. Together, these controls demonstrate how effective security governance combines technical safeguards with clear ownership, monitoring, and accountability to reduce the likelihood and potential impact of a major security incident.








Part 4: Developing Security Governance Metrics and Reporting
SECURITY GOVERNANCE METRIC SCRIPT
<img width="645" height="61" alt="Screenshot 2026-10-07 192754" src="https://github.com/user-attachments/assets/04c33cc1-3cf9-4e58-a5bc-009c338cb768" />

EXECUTIVE DASHBOARD HTML FILE
<img width="803" height="63" alt="Screenshot 2026-10-07 192900" src="https://github.com/user-attachments/assets/10156e0d-fd1f-442f-8302-c3dd72890f27" />


THE BOARD REPORT
<img width="1343" height="551" alt="Screenshot 2026-10-07 193014" src="https://github.com/user-attachments/assets/bb587d4c-6d0a-400e-aeaa-bd9009f91009" />
<img width="1362" height="566" alt="Screenshot 2026-10-07 193031" src="https://github.com/user-attachments/assets/eb63440d-fa7c-4bd5-95f5-346df27ab64f" />


THE METRIC FRAMEWORK DOCUMENT
<img width="822" height="63" alt="Screenshot 2026-10-07 193120" src="https://github.com/user-attachments/assets/19340518-df19-4f89-9457-45f6a640dc36" />
<img width="1358" height="534" alt="Screenshot 2026-10-07 193818" src="https://github.com/user-attachments/assets/0d7db72a-0426-4ac3-9aaf-9764a096478f" />
<img width="929" height="538" alt="Screenshot 2026-10-07 193837" src="https://github.com/user-attachments/assets/d8278237-b9b2-4924-9b92-c5b90f2adf46" />
<img width="1048" height="528" alt="Screenshot 2026-10-07 193853" src="https://github.com/user-attachments/assets/ef0ae4c7-e78c-417d-9d6c-456802403b12" />
<img width="1365" height="488" alt="Screenshot 2026-10-07 193906" src="https://github.com/user-attachments/assets/e65ced02-f069-4616-b931-936f0335e0df" />



THE DASHBOARD USER GUIDE
<img width="1358" height="550" alt="Screenshot 2026-10-07 194105" src="https://github.com/user-attachments/assets/836e687e-9d10-453b-9666-f70ae4f0204c" />
<img width="1032" height="554" alt="Screenshot 2026-10-07 194122" src="https://github.com/user-attachments/assets/1b21cd62-d013-4f99-b470-719d7915f84c" />
<img width="1359" height="535" alt="Screenshot 2026-10-07 194230" src="https://github.com/user-attachments/assets/aaa1fc2d-7ba6-4de9-bd62-9ac3eed206da" />



6. Screenshot of the Executive Dashboard
  <img width="1361" height="566" alt="Screenshot 2026-10-07 172934" src="https://github.com/user-attachments/assets/2808e729-b4e4-4a9e-a218-3e566b5a998c" />
<img width="1338" height="491" alt="Screenshot 2026-10-07 172948" src="https://github.com/user-attachments/assets/fe1313c4-e1ae-43c2-aafb-a32399826106" />
<img width="1317" height="472" alt="Screenshot 2026-10-07 173000" src="https://github.com/user-attachments/assets/c5373c58-6e77-492c-84ba-a5e82a7fa2da" />
<img width="1347" height="472" alt="Screenshot 2026-10-07 173013" src="https://github.com/user-attachments/assets/3e9837c8-60b5-4727-87f5-1465dc19d96e" />




8. Screenshots of the visualizations 
<img width="773" height="139" alt="Screenshot 2026-10-07 194549" src="https://github.com/user-attachments/assets/faadb28e-c66e-4a47-bba7-c998b7b7177c" />
<img width="1361" height="614" alt="Screenshot 2026-10-07 195449" src="https://github.com/user-attachments/assets/bb3991b8-314a-466d-a0eb-bcaaea8d76fa" />

<img width="1350" height="608" alt="Screenshot 2026-10-07 195525" src="https://github.com/user-attachments/assets/f7919290-5ee2-4407-bdae-817447c6d745" />

<img width="1364" height="617" alt="Screenshot 2026-10-07 195552" src="https://github.com/user-attachments/assets/88ac3c80-eb9d-46be-a1e4-72514146ea41" />

<img width="1354" height="617" alt="Screenshot 2026-10-07 195613" src="https://github.com/user-attachments/assets/fad29da5-441e-4b8c-a3b1-a8f4ba9f9afa" />

<img width="1361" height="611" alt="Screenshot 2026-10-07 195635" src="https://github.com/user-attachments/assets/5d0d0c58-0024-4327-873c-c7e1a21ecec2" />


9. HOW METRICS AND REPORTING MECHANISMS SUPPORT EFFECTIVE SECURITY GOVERNANCE
The security governance metrics and reporting mechanisms provide management with measurable information about the organization’s security posture, control performance, compliance status, and security trends. Metrics such as patch compliance, vulnerability remediation, security incidents, security monitoring coverage, and policy compliance help identify weaknesses and track whether security controls are achieving their intended objectives. The executive dashboard presents this information in a consolidated format, allowing management to quickly identify areas requiring attention and prioritize corrective actions.
The board report and operational metrics also support governance oversight by providing regular information for decision-making, accountability, and continuous improvement. By assigning metrics to defined targets, owners, reporting frequencies, and audiences, the organization can monitor progress over time, identify emerging risks, and ensure that security governance decisions are supported by measurable evidence.        






