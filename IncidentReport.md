## Incident report analysis

### Summary
The organization recently experienced a DDoS attack, which compromised the internal network for two hours until it was resolved.
During the attack, the organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services. 
The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack

### Identify
The incident management team found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack

### Protect
The team configured a new protective firewall and will invest in an intrusion prevention system. 

### Detect
To detect further successful attacks the team will use a firewall logging tool, configure source IP address verification into the firewall and perform regular penetration testing to ensure no such vulnerabilities are repeated. 

### Respond
The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services. 

### Recover
Access to network services needs to be restored to full functioning state. External ICMP flood attacks should be blocked by the firewall in the future. All non-critical network services should be shut down first, then critical services restored. Once incoming ICMP packets have timed out, all non-critical services and systems can be brought back online. 


