# Final Phishing Campaign Simulation (Ethical Lab)

## Overview
This project documents a **controlled, ethical phishing campaign simulation** conducted for learning and defensive awareness purposes. The objective was to understand how phishing campaigns are designed, executed, and measured, while also highlighting **why modern email defenses successfully block unauthenticated attacks**.

No real users were targeted, and no real credentials were collected.

---

## Tools Used
- GoPhish – campaign management, landing pages, email templates, reporting  
- Postfix (Localhost) – local mail transfer agent for test delivery  
- Kali Linux – attack simulation environment  
- HTML – landing page content  
- Temporary email service – test mailbox (non-production)

---

## Campaign Scope
The campaign simulated a **real-world phishing workflow** from an attacker’s perspective, including:
- Designing a believable phishing email template  
- Creating a landing page that mimics a legitimate login flow  
- Configuring a sending profile using a local SMTP server  
- Grouping test users and launching a controlled campaign  
- Observing user interaction metrics from the GoPhish dashboard  

---

## Campaign Configuration
- **Email Template:** Imported and modified from a real spam email sample  
- **Landing Page:** Custom HTML page configured to simulate a credential prompt  
- **Sending Profile:** Postfix on `localhost:25`  
- **Target Group:** Single test user created with a temporary email address  
- **Tracking Enabled:** Email opens, link clicks, and page visits  

> Credential capture was intentionally disabled to maintain ethical boundaries.

---

## Observations & Results
The GoPhish dashboard successfully tracked:
- Email delivery attempts  
- Email opens  
- Link clicks  
- Landing page visits  

When tested against modern email providers (e.g. Outlook), emails sent from a local unauthenticated server were blocked. This demonstrated the effectiveness of **SPF, DKIM, and DMARC enforcement** in real-world environments.

---

## Key Learning Outcomes
- Phishing campaigns rely heavily on **social engineering**, not just tools  
- Even well-crafted phishing emails fail without proper email authentication  
- Modern email security controls significantly reduce spoofing success rates  

Understanding attacker workflows helps defenders:
- Identify weak points in email security  
- Improve security awareness training  
- Tune detection and response mechanisms  

---

## Limitations
Full email header analysis (SPF/DKIM/DMARC) could not be performed due to mail rejection by major providers. This limitation reflects **real-world defensive controls**, not a misconfiguration.

---

## Ethical Disclaimer
This project was conducted **strictly for educational and defensive learning purposes**.  
No real individuals, organizations, or production systems were targeted.  
The techniques demonstrated should **never be used maliciously**.

---

## Why This Project Matters
This simulation bridges the gap between:
- Theoretical phishing knowledge  
- Practical attacker methodology  
- Real-world defensive effectiveness  

It emphasizes not just *how phishing is done*, but *why many attacks fail* — a critical perspective for security analysts.
