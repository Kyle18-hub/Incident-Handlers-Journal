# Incident Handler’s Journal
Incident Summary:  
Date: 2024-09-15  
Time of Detection: 14:30 UTC  
Incident Name: Unauthorized Network Access Attempt (Incident #165)  
Detection Method: SIEM Alert triggered for unusual outbound traffic.  
Incident Type: Network intrusion  
Severity: High  

# Incident Timeline

**[15-09-2024, 14:30 UTC]**: SIEM alert triggered for abnormal outbound traffic to suspicious IP (203.0.113.45) from internal workstation (192.168.1.12).

**[15-09-2024, 14:35 UTC]**: SOC Analyst begins initial investigation. Traffic logs reviewed; suspicious pattern indicates possible data exfiltration attempt.

**[15-09-20245, 14:50 UTC]**: Initial containment initiated. Firewall rules updated to block outbound traffic to suspicious IP.

**[15-09-2024, 15:10 UTC]**: Endpoint protection scan initiated on workstation. Malicious PowerShell script identified and quarantined.

**[15-09-2024, 15:30 UTC]**: Security Incident Response Team (SIRT) notified for further investigation.

**[15-09-2024, 15:45 UTC]**: Memory dump and forensic analysis initiated. Indicators of compromise (IOCs) gathered.
# Root Cause

**Initial Intrusion Vector:** Phishing email containing malicious link, delivered to user on internal workstation (192.168.1.12). User executed the link, leading to the download of a PowerShell-based malware.

**Vulnerability:** User unaware of phishing attempt, lack of multi-factor authentication (MFA) for email system.

**Mitigation Efforts:**
1. Blocked malicious IP address (203.0.113.45).
2. Isolated affected workstation for further forensic analysis.
3. Initiated organization-wide awareness training for phishing prevention.
# Post-Incident Actions

**Immediate Actions:**
1. Perform deep scan of the network for lateral movement and other affected systems.
2. Block further outbound connections to known malicious IP ranges.
3. Review endpoint logs and identify any abnormal user behaviors.

**Long-Term Actions:**
1. Implement multi-factor authentication (MFA) for email and remote access.
2. Review and strengthen security policies around email attachments and links.
3. Update firewall and IDS/IPS rules for enhanced monitoring of outbound traffic.
4. Schedule company-wide cybersecurity training focusing on phishing and social engineering.

**Incident Closure:** Pending completion of action items.
# Key Lessons

1. **Importance of Proactive Threat Detection:** The incident was identified by a SIEM alert due to unusual traffic patterns. This emphasizes the value of network monitoring tools.
2. **User Education:** The initial point of failure was a phishing email, underlining the importance of regular training and awareness for all employees.
3. **Quick Containment:** Blocking the IP quickly prevented further data exfiltration, demonstrating the effectiveness of prompt response actions.

*please note that this was a fictional incident
