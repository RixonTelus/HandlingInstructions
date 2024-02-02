Investigation Notes - to review once sample is present

**INCIDENT HAS NOT TRIGGERED PREVIOUSLY - HANDLING INSTRUCTIONS NOT ACCURATE. REACH OUT TO T2 TO ADVISE THIS USE-CASE HAS TRIGGERED**

Review Incident --> Full Details page; are there any alerts related to the account, IP, host? "Investigate" function can be used to investigate each entity present in the alert. 

In the events, take note of:

xxxxxx

 

Leverage the Investigation Insights workbook, entity behaviour, and KQL Sign-in query (SecurityEvent | where IPAddress == “XXX”)  to gather more details on the user and IP. 

Investigate User: 
Use the “Investigation Insights” workbook & Entity Behaviour function to find relevant context for the associated account

Look for location anomalies, IOCs, etc., that could indicate account compromise 

Using the Azure AD Audit logs workbook, filter the users to view other actions performed by them around the time of detection

Investigate Account(s)

Did the account conduct any other suspicious behavior, or trigger other alerts?

Use KQL: (SecurityEvent | where Account == “XXX”)

Investigate IP Address
Leverage OSINT resources

Is this IP used by multiple users?

Is the IP typically associated with the account?

Were they successfully authenticated through MFA?

Any failures or other suspicious patterns?

Use KQL: (SecurityEvent | where IPAddress == “XXX”)

 

Escalate this alert along with all relevant data if you are unable to confirm the login activity is legitimate, or if there are signs of malicious compromise.

KQL

Run relevant hunting queries - dig through the list of available Hunting queries applicable to see if there are signs of potential threats related -  (set favorite queries by clicking the star). Attach any bookmark to the incident if it provides insights and share them
