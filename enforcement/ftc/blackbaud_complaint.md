2023181

UNITED STATES OF AMERICA BEFORE THE FEDERAL TRADE COMMISSION

COMMISSIONERS:	Lina M. Khan, Chair Rebecca Kelly Slaughter Alvaro M. Bedoya

DOCKET NO.

# COMPLAINT

The Federal Trade Commission, having reason to believe that Blackbaud, Inc., a corporation, (“Blackbaud”), has violated the provisions of the Federal Trade Commission Act, 15 U.S.C. § 45, and it appearing to the Commission that this proceeding is in the public interest, alleges:

**1.**	Respondent Blackbaud, Inc. is a Delaware corporation with its principal place of business at 65 Fairchild Street, Charleston, South Carolina 29492.

**2.**	The acts and practices of Blackbaud alleged in this complaint have been in or affecting commerce, as “commerce” is defined in Section 4 of the Federal Trade Commission Act, and constitute unfair and/or deceptive acts or practices, in or affecting commerce, in violation of Section 5(a) of the Federal Trade Commission Act.

## Summary of the Case

**3.**	Blackbaud failed to use appropriate information security practices to protect consumers’ personal information. These failures allowed an attacker to access Blackbaud’s customer databases and steal personal information relating to millions U.S. consumers, as described in greater detail below.

Blackbaud’s Business Practices

**4.**	Blackbaud provides a variety of data services and financial, fundraising, and administrative software services to its customers, more than 45,000 companies, nonprofits, foundations, educational institutions, healthcare organizations, and individual consumers throughout the U.S. and abroad. It maintains a wide variety of consumers’ personal information on behalf of its customers, as described below in Paragraph 8.

**5.**	Blackbaud generates most of its U.S. revenues primarily from software solutions in cloud and hosted environments; payment and transaction services; software maintenance and support services; and professional services, including implementation, consulting, training, and analytic services. It earned annual revenues of approximately $1.1 billion in 2022.

## Data Breach

**6.**	On February 7, 2020, an attacker gained access to Blackbaud’s self-hosted legacy product databases. The attacker remained undetected for over three months, until May 20, 2020, when a member of Blackbaud’s engineering team identified a suspicious login on a backup server. By the time Blackbaud discovered the breach, the attacker had stolen data from tens of thousands of Blackbaud’s customers, which comprised of the personal information of millions of consumers.

**7.**	The attacker purportedly used a Blackbaud customer’s login and password to access the customer’s Blackbaud-hosted database. Once logged in, the attacker was able to freely move across multiple Blackbaud-hosted environments by leveraging existing vulnerabilities and local administrator accounts, subsequently creating new administrator accounts and ultimately exfiltrating massive amounts of consumer data belonging to Blackbaud’s customers.

**8.**	Blackbaud’s investigation found that the attacker had exfiltrated files in which millions of consumers’ personal information was not encrypted, including consumers’ full names, age, date of birth, social security numbers, home addresses, phone numbers, email addresses, financial information (including bank account information, estimated wealth, and identified assets), medical information (including patient and medical record identifiers, treating physician names, health insurance information, medical visit dates, and reasons for seeking medical treatment), gender, religious beliefs, marital status, spouse names, spouses’ donation history, employment information (including salary) educational information, and account credentials.

**9.**	Blackbaud’s deficient encryption practices magnified the severity of the data breach. For example, Blackbaud allowed customers to store social security numbers and bank account information in unencrypted fields not specifically designated for those purposes. It also allowed customers to upload attachments containing consumers’ personal information, which Blackbaud did not encrypt. Finally, Blackbaud did not encrypt its database backup files which contained complete customer records from the products’ databases, even for former customers.

**10.**	Blackbaud’s failure to implement appropriate data retention policies further exacerbated the severity of the breach. Blackbaud did not enforce its own data retention policies, resulting in the company keeping customer’s consumer data for years longer than was necessary. Incredibly, in some instances, Blackbaud retained data belonging to former customers, customers who had switched to products not affected by the breach, and even potential customers for years longer than was necessary.

**11.**	Once detected, the attacker threatened to expose the stolen consumer data unless Blackbaud paid a ransom. Blackbaud eventually agreed to pay 24 Bitcoin (valued at $235,000 at the time) in exchange for the attacker’s promise to delete the stolen data. Blackbaud has not been able to conclusively verify that the attacker deleted the stolen data.

## Blackbaud’s Deceptive Breach Notification Statements

**12.**	Blackbaud failed to notify its customers of the breach for two months after detection. It issued its first notice to its customers on July 16, 2020.

**13.**	However, in its July 2020 breach notification, Blackbaud misrepresented the scope and severity of the breach after conducting an exceedingly inadequate investigation. Blackbaud stated in its communications to customers:

The cybercriminal did not access credit card information, bank account information, or social security numbers. . .

No action is required on your end because no personal information about your constituents was accessed. (emphasis in original)

(Exhibit A, Sample Blackbaud Customer Breach Notification (July 16, 2020))

**14.**	Although Blackbaud knew, as early as July 31, 2020, as part of its continuing post-breach investigation, that the attacker had exfiltrated consumers’ bank account numbers and social security numbers, Blackbaud did not disclose the extent of the breach to its customers until October 2020.

**15.**	Blackbaud’s deceptive statements, combined with the months’ long delay in providing accurate notice about the breach, led many customers to believe that notification to their consumers was unnecessary. Due to this delay in notice, consumers suffered additional harm because they had no way to know that they needed to take any mitigating steps to protect themselves from identity theft.

**16.**	Since the breach, Blackbaud has received multiple complaints from consumers involving attempted identity theft and fraud using the personal information exposed in the breach (e.g., credit card, tax, and unemployment fraud). Blackbaud has since offered credit monitoring services to a limited subset of affected customers.

## Blackbaud’s Deceptive Information Security Statements

**17.**	Blackbaud has made explicit representations about its information security practices that led customers to believe that it used reasonable and appropriate information security practices to protect consumers’ personal information.

**18.**	Blackbaud’s Privacy Policy on its website, dated December 17, 2019, included the following statement:

Security of your Personal Information. We restrict access to personal information collected about you at our website to our employees, our affiliates’ employees, those who are otherwise specified in this Policy or others who need to know that information to provide the Services to you or in the course of conducting our business operations or activities. While no website can guarantee exhaustive security, we maintain appropriate physical, electronic and procedural safeguards to protect your personal information collected via the website. We protect our databases with various physical, technical and procedural measures and we restrict access to your information by unauthorized persons. We also advise all Blackbaud employees about their responsibility to protect customer data and we provide them with appropriate guidelines for adhering to our company’s business ethics standards and confidentiality policies. Inside Blackbaud, data is stored in password-controlled servers with limited access.

(Exhibit B, Blackbaud.com, Privacy Policy North America (December 17, 2019))

## Blackbaud’s Information Security Practices

**19.**	Blackbaud failed to provide reasonable or appropriate security for the personal information that they collected and maintained about consumers. Among other things, Blackbaud failed to:

a.	Implement appropriate password controls. As a result of this failure, employees often used default, weak, or identical passwords;

b.	Apply adequate multifactor authentication for both employees and customers to protect sensitive consumer information. For example, Blackbaud failed to comply with industry standards and internal policies requiring multifactor authentication for remote access to sensitive environments;

c.	Prevent data theft by monitoring for unauthorized attempts to transfer or exfiltrate consumers’ personal information outside the company’s networks; continuously log and monitor its systems and assets to identify data security events; and perform regular assessments as to the effectiveness of protection measures;

d.	Implement and enforce appropriate data retention schedules and deletion practices for the vast amounts of consumers’ personal information stored on its network;

e.	Patch outdated software and systems in a timely manner, leaving Respondents’ networks susceptible to attacks;

f.	Test, audit, assess, or review its products’ or applications’ security features; and conduct regular risk assessments, vulnerability scans, and penetration testing of its networks and databases;

g.	Implement appropriate firewall controls. This failure resulted in an attacker making unauthorized connections from outside of Respondents’ networks; and

h.	Implement appropriate network segmentation to prevent attackers from moving freely across Blackbaud’s networks and databases.

## The Impact of Blackbaud’s Failures on Consumers

**20.**	Respondent’s failures to provide reasonable security for the sensitive, personal consumer information they collected, transmitted, and stored has caused or is likely to cause substantial injury to consumers.

**21.**	Additionally, Blackbaud’s failure to accurately communicate the scope and severity of the breach in its initial notification to its customers caused or is likely to cause substantial injury to consumers because they were not able to mitigate the effects of the breach in a timely manner.

**22.**	Consumers have also suffered, and will continue to suffer, additional injuries due to the significant amount of highly detailed and individualized personal information exposed.

**23.**	Blackbaud could have prevented or mitigated these failures described in Paragraph 19 through well known, readily available, relatively low-cost measures. For example, Blackbaud could have required regular review of access permissions, enabled multi- factor authentication for all employees and customers, and implemented reasonable data retention practices. Any of these measures would likely have prevented the May 2020 breach or, at minimum, lessened its impact.

**24.**	These harms were not reasonably avoidable by consumers, as consumers had no way to know about Respondents’ information security failures described in Paragraph 19 above.

## Violation of the FTC Act

**25.**	The acts and practices of Respondent, as alleged in this Complaint, constitute unfair and/or deceptive acts or practices, in or affecting commerce, in violation of Section 5(a) of the Federal Trade Commission Act.

### Count I – Blackbaud’s Unfair Information Security Practices

**26.**	Through the means described in Paragraphs 6 to 11 and 19-24, Blackbaud failed to take reasonable steps to prevent unauthorized access to sensitive consumer data maintained by its customers on its network.

**27.**	Blackbaud’s actions caused or are likely to cause substantial injury to consumers that consumers cannot reasonably avoid themselves and that is not outweighed by countervailing benefits to consumers or competition.

**28.**	Therefore, Blackbaud’s practices as described in Paragraph 19 above constitute unfair acts or practices in violation of Section 5 of the FTC Act, 15 U.S.C. §§ 45(a) and 45(n).

### Count II – Blackbaud’s Unfair Data Retention Practices

**29.**	Through the means described in Paragraph 10, Blackbaud failed to implement and enforce reasonable data retention practices for sensitive consumer data maintained by its customers on its network.

**30.**	Blackbaud’s actions caused or are likely to cause substantial injury to consumers that consumers cannot reasonably avoid themselves and that is not outweighed by countervailing benefits to consumers or competition.

**31.**	Therefore, Blackbaud’s practices as described in Paragraph 19(d) above constitute unfair acts or practices in violation of Section 5 of the FTC Act, 15 U.S.C. §§ 45(a) and 45(n).

### Count III—Blackbaud’s Unfair Inaccurate Breach Notification

**32.**	Through the means described in Paragraphs 12 to 16 and 21, Blackbaud failed to accurately communicate the scope and severity of the breach in its initial notification to customers.

**33.**	Blackbaud’s actions caused or are likely to cause substantial injury to consumers that consumers cannot reasonably avoid themselves and that is not outweighed by countervailing benefits to consumer or competition.

**34.**	Therefore, Blackbaud’s practices described in Paragraphs 12 and 13 above constitute unfair acts or practices in violation of Section 5 of the FTC Act, 15 U.S.C. §§ 45(a) and 45(n).

### Count IV – Blackbaud’s Deceptive Security Statements

**35.**	Through the means described in Paragraphs 17 to 18, Blackbaud has represented, directly or indirectly, expressly or by implication, that they used appropriate safeguards to protect consumers’ personal information.

**36.**	In truth and in fact, as set forth in Paragraph 19, Blackbaud did not maintain appropriate safeguards to protect consumers’ personal information. Therefore, the representation set forth in Paragraph 18 is false or misleading.

### Count V – Blackbaud’s Deceptive Initial Breach Notification

**37.**	Through the means described in Paragraph 12 to 13, Blackbaud has represented, directly or indirectly, expressly or by implication, that consumers’ personal information had not been subject to the breach in its first notification.

**38.**	In truth and in fact, as set forth in Paragraphs 14 to 16, consumers’ personal information had been exfiltrated by the attacker in the breach. Therefore, the representation set forth in Paragraph 13 is false or misleading.

THEREFORE, the Federal Trade Commission this    day of    2023 has issued this complaint against Respondent.

SEAL:

By the Commission.



April J. Tabor Secretary

