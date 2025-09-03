# GitSync

## Integrations
|Name|Description|
|----|-----------|
|Google Chronicle|Google SecOps enables you to examine the aggregated security information for your enterprise going back for months or longer. Use Google SecOps to search across all of the domains accessed from within your enterprise. To enable the Google API client to communicate with the Backstory API you will need Google Developer Service Account Credential, https://developers.google.com/identity/protocols/OAuth2#serviceaccount.|
|Jira|Jira Software is part of a family of products designed to help teams of all types manage work. Originally, Jira was designed as a bug and issue tracker. But today, Jira has evolved into a powerful work management tool for all kinds of use cases, from requirements and test case management to agile software development. Jira will be the perfect fit for: requirements & test case management, agile teams, project management teams, software development teams, product management teams, task management, bug tracking and much more...|
|QRadar|IBM QRadar is an enterprise security information and event management (SIEM) product. It collects log data from an enterprise, its network devices, host assets and operating systems, applications, vulnerabilities, and user activities and behaviors.|
|Siemplify|Google SecOps integration package includes all of Google SecOps's internal actions, jobs etc.|


## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|Google Chronicle - Chronicle Alerts Connector|Pull information about Rule based alerts from Google Chronicle. Note: dynamic list is used for filtering purposes. For all of the details please visit the documentation portal.|True|
|Qradar Correlation Events Connector V2|Fetches Qradar offenses and forms Chronicle SOAR (CSOAR) alerts for each Qradar rule added to dynamic list in CSOAR. Connector fetches only the offenses for rules that are added to CSOAR dynamic list. Connector requires minimum Qradar API version 10.1. Connector creates CSOAR alerts based on the rule name of Qradar offense, not the offense name.|True|


## Playbooks
|Name|Description|
|----|-----------|
|New Playbook||


## Jobs
|Name|Description|
|----|-----------|
|Dummy Job||
|Sync Comments|Sync comments between Google SecOps alert's case and corresponding Jira ticket. Sync mechanism works in both ways, Google SecOps → Jira and Jira → Google SecOps|
|instance 1||
|renamed instance 1||

