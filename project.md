# **Phishing Attack Simulation with GoPhish**

## **1. Introduction**
Phishing is one of the most prevalent cybersecurity threats, leveraging social engineering techniques to trick users into revealing sensitive information. This project simulates a real-world phishing attack using **GoPhish**, an open-source phishing simulation tool, to understand its features, assess user susceptibility, and explore mitigation strategies.

## **2. Objective**
The primary goal of this project was to:
- **Test GoPhish's capabilities** in creating and managing phishing campaigns.
- **Explore different phishing techniques**, including email spoofing and cloned landing pages.
- **Analyze user behavior** when interacting with phishing emails.
- **Understand mitigation strategies** to prevent real-world phishing attacks.

## **3. Project Setup**

### **3.1 Environment**
- **GoPhish Deployment:** Hosted on **Railway**, deployed from a forked GitHub repository.
- **SMTP Server:** Configured using **SendGrid** to send phishing emails.
- **Targeted Users:** Not sent to real users; only tested within a controlled environment.

### **3.2 Email Phishing Scenario**
- **Theme:** Fake password reset request for **Latch** users.
- **Email Template:**
  - Copied a legitimate Latch password reset email.
  - Modified contents to request a password reset every **6 months due to security policies**.
  - Embedded a **malicious link** to the phishing landing page.
- **Landing Page:**
  - Cloned Latch’s official password reset page.
  - Added an extra field for **old password**, intending to capture credentials.
  - Redirected users to a fake reset confirmation page before sending them to the real Latch website.

## **4. Execution and Findings**
- Explored **all possible user actions**, including email interaction and credential submission.
- **Challenges Faced:**
  - SMTP sending profile configuration issues.
  - **SendGrid domain restrictions**, making email delivery inconsistent.
  - Emails landed in **spam folders** by default due to sender verification failures.
- **Expected User Response:**
  - Ideally, users should recognize the email as **phishing** and report it.
  - Users should notice **incorrect sender addresses** and **suspicious URLs**.

## **5. Key Takeaways and Mitigation Strategies**
### **5.1 Identifying Phishing Emails**
- **Check sender address:** Verify that emails come from trusted domains.
- **Inspect links before clicking:** Hover over links to see the real destination.
- **Look for spelling errors & design flaws:** While not always present, these are common red flags.
- **Be cautious with urgency-based messages:** Phishing emails often use psychological pressure.

### **5.2 Technical Defenses**
- **Enable Multi-Factor Authentication (MFA):** Reduces risk even if credentials are compromised.
- **Use Email Filtering Solutions:** Employ tools like SPF, DKIM, and DMARC to block spoofed emails.
- **Train Employees & Users:** Regular security awareness training helps reduce phishing success rates.
- **Monitor Network Activity:** Detect unusual login attempts and prevent credential misuse.

## **6. Conclusion**
This project provided hands-on experience with GoPhish and demonstrated how phishing campaigns are executed and detected. The findings reinforce the importance of **cybersecurity awareness training**, **technical email security measures**, and **critical thinking before interacting with suspicious emails**.

### **7. Future Work**
- Deploy the campaign to **a test group of users** and analyze real-world responses.
- Experiment with **advanced evasion techniques** (e.g., URL redirection, obfuscated payloads).
- Explore **automated phishing detection** tools to counter such attacks.

---
### **Project Artifacts:**
- **Screenshots:** 
- **Landing page:**
- **Redirect page:**

