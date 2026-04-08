# Real-World Log Investigation

## 🚨 Scenario
A simulated security alert was triggered in a SOC environment due to multiple failed login attempts followed by a successful login from an unfamiliar IP address.

---

## 🎯 Objective
Determine whether this activity represents a legitimate login or a potential account compromise.

---

## 🛠️ Tools Used
- Log analysis (simulated)
- SIEM concepts
- Basic networking knowledge

---

## 🔍 Investigation Steps

1. Reviewed login logs for failed attempts  
2. Identified repeated failures from same IP address  
3. Detected successful login immediately after failed attempts  
4. Observed that failed attempts occurred within a short time window (indicative of automated attack behavior)  
5. Compared login behavior against normal patterns  
6. Reviewed IP origin for anomalies  

---

## 🧠 Analysis

- Multiple failed login attempts indicate a possible brute force attack  
- Successful login after repeated failures suggests credential compromise  
- IP address was not previously associated with the user  
- Potential risk of unauthorized access to sensitive systems or data if not mitigated  

---

## 🚨 Decision

Classified as a **True Positive (Potential Account Compromise)** and escalated according to incident response procedures.

---

## 🔐 Recommended Actions

- Force password reset  
- Enable multi-factor authentication (MFA)  
- Block suspicious IP address  
- Monitor account activity  

---

## 📌 Key Takeaways

- Demonstrated ability to analyze logs and detect suspicious patterns  
- Differentiated between normal activity and potential threats  
- Applied structured investigation process  
- Made clear escalation decision  

---

## 🎥 Video Walkthrough

Demonstration of full investigation process and decision-making:

Owner avatar
real-world-log-investigation
Public
techByMarcus/real-world-log-investigation
Go to file
t
Name		
techByMarcus
techByMarcus
Add files via upload
00d3ce3
 · 
now
README.md
Revise README for clarity and consistency
11 hours ago
finalsimpresentation.mp4
Add files via upload
now
Repository files navigation
README
Real-World Log Investigation
🚨 Scenario
A simulated security alert was triggered in a SOC environment due to multiple failed login attempts followed by a successful login from an unfamiliar IP address.

🎯 Objective
Determine whether this activity represents a legitimate login or a potential account compromise.

🛠️ Tools Used
Log analysis (simulated)
SIEM concepts
Basic networking knowledge
🔍 Investigation Steps
Reviewed login logs for failed attempts
Identified repeated failures from same IP address
Detected successful login immediately after failed attempts
Observed that failed attempts occurred within a short time window (indicative of automated attack behavior)
Compared login behavior against normal patterns
Reviewed IP origin for anomalies
🧠 Analysis
Multiple failed login attempts indicate a possible brute force attack
Successful login after repeated failures suggests credential compromise
IP address was not previously associated with the user
Potential risk of unauthorized access to sensitive systems or data if not mitigated
🚨 Decision
Classified as a True Positive (Potential Account Compromise) and escalated according to incident response procedures.

🔐 Recommended Actions
Force password reset
Enable multi-factor authentication (MFA)
Block suspicious IP address
Monitor account activity
📌 Key Takeaways
Demonstrated ability to analyze logs and detect suspicious patterns
Differentiated between normal activity and potential threats
Applied structured investigation process
Made clear escalation decision
🎥 Video Walkthrough
Demonstration of full investigation process and decision-making

[Watch the Walkthrough]

