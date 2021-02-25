# Rules of Engagement

When performing application security analysis, it is expected that the tester follow the *Rules of Engagement* as laid out below. This is to standardize the scope of application testing and provide a concrete awareness of what is considered "out of scope" for security analysis.

## Rules of Engagement - For those requesting review

* Web Application Firewall (WAF) is managed centrally by Swift Office but automatic port blocking is enabled. This can greatly slow down a person performing the any security test.
* Similarly, if a service is running on a virtual machine, ensure services such as `fail2ban` are disabled.
* You cannot make changes to the running application until the test is complete. This is to prevent accidentally breaking an otherwise valid attack in progress.
* Any review results are not considered as "final". A security review should always be performed by a security team orchestrated by the Republic of Singapore Air Force (RSAF) Central Team prior to moving an application into production. If a project team requires further assistance, they can engage RSAF Central Team for assistance.

## Rules of Engagement - For those performing tests

* Do not attempt to perform Denial-of-Service attacks or otherwise crash services on Swift Commercial Cloud. Heavy active scanning is tolerated (and is assumed to be somewhat of a load test) but deliberate takedowns are not permitted.
* Do not interact with human beings. Phishing credentials or other such client-side attacks are off-limits. Detailing XSS and similar attacks is encouraged as a part of the test, but do not leverage these against internal users or customers.
* Attack from a single point. Especially if the application is currently in the customer's hands, provide the IP address or hostname of the attacking host to avoid setting off alarms.
