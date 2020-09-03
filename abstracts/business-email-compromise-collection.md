---
uuid: b765456f-a22d-4236-8ea3-81bb3c08ebbe
created by: rhigham
created date: 09/02/2020
last ran: xx/xx/20xx
classification: collection
priority: 3
---

## Hypothesis
Threat Actors have gained access to one of more mailboxes and are using them to conduct transactions or exfiltrate sensitive information.

## Priority Explanation
Business email compromise has become common

## MITRE Reference(s)
* https://attack.mitre.org/techniques/T1114/003/
* https://attack.mitre.org/techniques/T1114/002/

## Threat Intel
* https://www.sans.org/blog/sans-data-incident-2020-indicators-of-compromise/
* https://www.agari.com/email-security-blog/business-email-compromise-bec-coronavirus-covid-19/

## Analytics
An analytic is logic that when applied to data produces actionable or otherwise relevant information.    
Separate each analytic with 3 hash marks and the word Analytic followed by the next sequential number 1, 2, 3, etc.

### Analytic 1 - Mailbox Rules - Office Activity Logs
* Look for rules that forward email to a suspicious/anomalous external email (exfil)
* Look for rules that forward email to an odd folder (staging)
* Look for rules that block or hide emails. e.g. prevent reporting suspiciuos email, signin from new device alerts, etc

### Analytic 2 - Mail flow rules (transport rules) - Exchange Online
* Look for rules that have been hidden in Microsoft Exchange

### Analytic 3 - Non-owner mailbox login activity

## Future Research
Non-owner mailbox login activity

## Reference Information:
https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules#:~:text=The%20main%20difference%20is%20mail,many%20types%20of%20messaging%20policies.
https://github.com/zolderio/microsoft/tree/master/Office365/ExchangeOnline/rules/mailRules

## Hunters Notes:
* As you iterate through this hunt, add any notes that might be helpful for the next time it is ran. 
* Every time a hunt is conducted, a new report should be created. 
* Include a link to the report of your findings in this section.
