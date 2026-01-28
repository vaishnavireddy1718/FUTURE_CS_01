# FUTURE_CS_01 – Vulnerability Assessment Report for a Live Website

 📌 Internship Information
- Intern Name: Arra Vaishnavi Reddy  
- Domain:Cyber Security  
- Organization:Future Interns  
- Task Name: Vulnerability Assessment Report for a Live Website  

🎯 Objective

The objective of this task is to perform a basic vulnerability assessment on a live web application using OWASP ZAP through a passive scanning approach. This task aims to identify common web security misconfigurations and vulnerabilities and understand their potential impact and remediation methods.

🛠 Tool Used
- OWASP ZAP (Zed Attack Proxy) – for passive web application security testing  
- Browser (ZAP Controlled Browser)  
- Canva – for designing the vulnerability assessment report  

🌐 Target Website
- URL: http://testphp.vulnweb.com  
- Assessment Type: Passive Scan  

Description:
The target website is an intentionally vulnerable web application created for security testing and educational purposes. It allows safe identification of vulnerabilities without affecting real-world production systems.

🧪 Steps Performed
1. Launched OWASP ZAP in Standard Mode  
2. Opened the ZAP controlled browser  
3. Accessed the target website through ZAP  
4. Browsed multiple pages of the application  
5. Allowed OWASP ZAP to perform passive scanning  
6. Reviewed and analyzed the generated security alerts  

👀 Observations
- The application traffic was successfully captured by OWASP ZAP  
- Passive scanning generated multiple security alerts  
- Missing security headers were commonly observed  
- No high-risk vulnerabilities were detected during the scan  

 ⚠️ Summary of Alerts
During the passive vulnerability assessment, OWASP ZAP detected a total of 10 security alerts , categorized as follows:
- 🔶 Medium Risk Alerts: 3  
- 🟡 Low Risk Alerts:5  
- 🔵 Informational Alerts: 2  

🚨Few Alerts

 1. Absence of Anti-CSRF Tokens
Risk Level:Medium

Description: 
The application does not implement Anti-CSRF tokens, making it vulnerable to Cross-Site Request Forgery attacks.

Impact: 
Attackers may perform unauthorized actions on behalf of authenticated users.

Mitigation: 
Implement Anti-CSRF tokens for all sensitive requests.

 2. Content Security Policy (CSP) Header Not Set
Risk Level:Medium  

Description:
The Content Security Policy header is missing, increasing the risk of Cross-Site Scripting (XSS) attacks.

Impact:  
Malicious scripts may be injected and executed in the user’s browser.

Mitigation:  
Configure and enforce a strict Content Security Policy header.

3. Missing Anti-Clickjacking Header
Risk Level: Medium  

Description:  
The application does not set the X-Frame-Options header.

Impact: 
The website may be embedded into malicious iframes, leading to clickjacking attacks.

Mitigation:  
Set the X-Frame-Options header or use the CSP frame-ancestors directive.

 4. X-Content-Type-Options Header Missing
Risk Level: Low  

Description:  
The X-Content-Type-Options header is not set to “nosniff”.

Impact: 
Browsers may incorrectly interpret content types, increasing XSS risks.

Mitigation:  
Set the X-Content-Type-Options header to “nosniff”.

5. Strict-Transport-Security Header Not Set
Risk Level: Low  

Description: 
The application does not enforce HTTPS using HSTS.

Impact: 
Users may be exposed to man-in-the-middle attacks.

Mitigation: 
Enable the Strict-Transport-Security header to enforce HTTPS connections.

⚠️ Risk Severity
- Overall Risk Level: Medium  

Justification:
Although the identified vulnerabilities were mostly of medium and low risk, they represent common security misconfigurations that could be exploited in real-world applications if left unaddressed.

 📉 Risk Impact
- Increased exposure to CSRF and XSS attacks  
- Possibility of clickjacking attacks  
- Weak enforcement of secure communication  
- Reduced overall security posture of the web application  

✅ Recommendations
- Implement Anti-CSRF protection mechanisms  
- Configure essential security headers  
- Enforce HTTPS and secure communication  
- Regularly perform vulnerability assessments  
- Follow web application security best practices  

🏁 Conclusion
This vulnerability assessment was conducted using OWASP ZAP on an intentionally vulnerable web application through a passive scanning approach. The assessment successfully identified multiple security misconfigurations, including missing security headers and the absence of Anti-CSRF protection.

Although the vulnerabilities were mostly of medium and low risk, they highlight common security weaknesses that can be exploited if left unaddressed. This task emphasized the importance of proactive security testing during the web application development lifecycle.

🔗 Repository Information
- Track Code:CS  
- Repository Name Format:FUTURE_CS_01  
- Internship Program: Future Interns Cyber Security Internship
