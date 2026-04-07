# Real-World Log Investigation

## 🚨 Scenario
A security alert was triggered due to multiple failed login attempts followed by a successful login from an unfamiliar IP address.

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
4. Compared login behavior against normal patterns  
5. Reviewed IP origin for anomalies  

---

## 🧠 Analysis

- Multiple failed login attempts indicate possible brute force attack  
- Successful login after repeated failures suggests credential compromise  
- IP address was not previously associated with the user  

---

## 🚨 Decision

**True Positive – Potential Account Compromise**

---

## 🔐 Recommended Actions

- Force password reset  
- Enable multi-factor authentication (MFA)  
- Block suspicious IP address  
- Monitor account activity  

---

## 📌 Key Takeaways

- Demonstrated ability to analyze logs and detect suspicious patterns  
- Differentiated between normal activity and potential threat  
- Applied structured investigation process  
- Made clear escalation decision  

---

## 🎥 Video Walkthrough

[Insert your OneDrive link here]
