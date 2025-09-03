<p align="center"><img src="./Resources/QRadar.svg" 
     alt="QRadar" width="200"/></p>

# QRadar

IBM QRadar is an enterprise security information and event management (SIEM) product. It collects log data from an enterprise, its network devices, host assets and operating systems, applications, vulnerabilities, and user activities and behaviors.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://x.x.x.x:port|
|API Token|None|True|Password|*****|
|API Version|None|True|String|10.1|


#### Dependencies
| |
|-|
|rsa-4.9-py3-none-any.whl|
|google_auth-2.33.0-py2.py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|cachetools-5.4.0-py3-none-any.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|TIPCommon-1.1.0.1-py2.py3-none-any.whl|


## Actions
#### List Reference Maps
List reference maps available in Qradar.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Fields To Return|Specify which fields should be returned by the action. If nothing is provided - return all available fields by default. Parameter accepts multiple values separated by comma.|False|String||
|Filter Condition|Specify a filter condition to return only specific elements, for example: element_type = ALNIC.|False|String||
|Number Of Elements To Return|Specify a maximum numbers of elements to return by the action.|True|String|25|



##### JSON Results
```json
[{"time_to_live":"3 years 3 mons 1 days 0 hours 10 mins 2.00 secs","timeout_type":"UNKNOWN","number_of_elements":0,"creation_time":1586153337161,"name":"User1","element_type":"ALNIC"},{"time_to_live":"3 years 0 mons 0 days 0 hours 10 mins 2.00 secs","timeout_type":"UNKNOWN","number_of_elements":1,"creation_time":1586153244122,"name":"User","element_type":"ALNIC"}]
```



#### List Reference Tables
List reference tables available in Qradar.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Fields To Return|Specify which fields should be returned by the action. If nothing is provided - return all available fields by default. Parameter accepts multiple values separated by comma.|False|String||
|Filter Condition|Specify a filter condition to return only specific elements, for example: element_type = ALNIC.|False|String||
|Number Of Elements To Return|Specify a maximum numbers of elements to return by the action.|True|String|25|



##### JSON Results
```json
[{"timeout_type":"UNKNOWN","number_of_elements":0,"creation_time":1612178717941,"name":"NewTable3","element_type":"IP"},{"timeout_type":"UNKNOWN","number_of_elements":0,"creation_time":1612178670650,"name":"NewTable2","element_type":"PORT"},{"timeout_type":"UNKNOWN","number_of_elements":0,"creation_time":1612178656238,"name":"NewTable1","element_type":"ALN"}]
```



#### Lookup for a Value in Reference Map of Sets
Check if a value is listed in a specific reference map of sets. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The name of the reference map of sets to check a value.|True|String||
|Value|The value to check in a referenced map of sets.|True|String||



##### JSON Results
```json
[{"last_seen":1583912905418,"key":"192.168.xxx.xxx","first_seen":1583912905418,"source":"reference data api","value":"jack"},{"last_seen":1612806496736,"key":"Key2","first_seen":1612806496736,"source":"reference data api","value":"jack"}]
```



#### Update Offense
Update Qradar Offense.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Offense ID|Offense ID to update.|True|String||
|Assigned To|User login to assign the offense to.|False|String||
|Status|New status of the offense.|True|List|Don't change|
|Closing Reason|If offense status will be set to closed, you will need to provide a Qradar closing reason.|False|String||
|Follow Up|Specify whether offense should be marked as a follow up.|False|Boolean|false|
|Protected|Specify whether offense should be marked as protected.|False|Boolean|false|



##### JSON Results
```json
{"last_persisted_time":1611143659000,"username_count":0,"description":"Web\n","rules":[{"id":100000,"type":"CRE_RULE"}],"event_count":0,"flow_count":4,"assigned_to":"admin","security_category_count":1,"follow_up":true,"source_address_ids":[50],"source_count":1,"inactive":true,"protected":true,"closing_user":null,"destination_networks":["other"],"source_network":"other","category_count":1,"close_time":null,"remote_destination_count":1,"start_time":1610451749000,"magnitude":0,"last_updated_time":1610451887000,"credibility":0,"id":1000,"categories":["Web"],"severity":0,"policy_category_count":0,"log_sources":[],"closing_reason_id":null,"device_count":0,"first_persisted_time":1610451722000,"offense_type":1,"relevance":0,"domain_id":0,"offense_source":"37.28.xxx.xxx","local_destination_address_ids":[],"local_destination_count":0,"status":"OPEN"}
```



#### Ping
Test connectivity to a Qradar instance
Timeout - 600 Seconds



#### Lookup for a Key in Reference Map of Sets
Check if a key is listed in a specific reference map of sets. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The name of the reference map of sets to check a key.|True|String||
|Key|The key to check in a referenced map of sets.|True|String||



##### JSON Results
```json
[{"last_seen":1583912905418,"key":"IP","first_seen":1583912905418,"source":"reference data api","value":"jack, john, huey"},{"last_seen":1612806496736,"key":"IP","first_seen":1612806496736,"source":"reference data api","value":"value2"}]
```



#### Lookup for a Key in Reference Map
Check if a key is listed in a specific reference map. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The name of the reference map to check a key.|True|String||
|Key|The key to check in a referenced map.|True|String||



##### JSON Results
```json
[{"last_seen":1586154232667,"key":"1001","first_seen":1586154232667,"source":"reference data api","value":"jack"}]
```



#### QRadar Simple AQL Search
Execute an AQL query based on parameters in QRadar.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Table Name|Specify what table should be queried.|True|List|Flows|
|Fields To Return|Specify what fields to return. If nothing is provided, action will return all fields.|False|String|*|
|Where Filter|Specify the WHERE filter for the query that needs to be executed. Note: you don't need to provide time filter, limiting and sorting. Also, you don't need to provide WHERE string in the payload.|False|String||
|Time Frame|Specify a time frame for the results. If "Custom" is selected, you also need to provide "Start Time".|False|List|Last Hour|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO-8601|False|String||
|End Time|Specify the end time for the results. Format: ISO-8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter will use current time.|False|String||
|Sort Field|Specify what parameter should be used for sorting.|False|String||
|Sort Order|Specify the order of sorting. Requires "Sort Field" to be provided.|False|List|ASC|
|Max Results To Return|Specify how many results to return. Default: 50.|False|String|50|



##### JSON Results
```json
{"flows":[{"destinationflags":"XX","destinationpackets":"X.X","sourcebytes":"XXX.X","protocolid":"X","sourceip":"XXX.XX.XXX.X","destinationbytes":"XXX.X","lastpackettime":"162845XXXXXXX","sourceflags":"XX","sourcepackets":"X.X","qid":"5325XXXX","flowtype":"X","destinationip":"XXX.XX.XXX.XXX","firstpackettime":"162845XXXXXXX","category":"XXXXX"}],"events":[{"starttime":"1628454727XXX","protocolid":"XXX","sourceip":"XXX.XX.XXX.XX","logsourceid":"XXX","qid":"XXXXXXX","sourceport":"X","eventcount":"X","magnitude":"X","identityip":"X.X.X.X","destinationip":"XXX.XX.XXX.XX","destinationport":"X","category":"XXXXX","username":"XXXXX"}]}
```



#### List Reference Sets
List reference sets available in Qradar.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Fields To Return|Specify which fields should be returned by the action. If nothing is provided - return all available fields by default. Parameter accepts multiple values separated by comma.|False|String||
|Filter Condition|Specify a filter condition to return only specific elements, for example: element_type = IP.|False|String||
|Number Of Elements To Return|Specify a maximum numbers of elements to return by the action.|True|String|25|



##### JSON Results
```json
[{"timeout_type":"FIRST_SEEN","number_of_elements":0,"creation_time":1440703855335,"name":"Windows Servers","element_type":"IP"},{"timeout_type":"FIRST_SEEN","number_of_elements":0,"creation_time":1440703724417,"name":"DHCP Servers","element_type":"IP"},{"time_to_live":"0 years 0 mons 7 days 0 hours 0 mins 0.00 secs","timeout_type":"LAST_SEEN","number_of_elements":0,"creation_time":1389036032886,"name":"Asset Reconciliation NetBIOS Blacklist","element_type":"ALNIC"}]
```



#### QRadar AQL Search
Run an arbitrary AQL query against the Qradar instance. The action returns an output in CSV format.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query Format|Query format to execute for example, “Select * from flows limit 10 last 10 minutes”.|True|String||



##### JSON Results
```json
{"events": [{"username": "None", "category": 4003, "starttime": 1548682790158, "destinationip": "1.1.1.1", "eventcount": 13, "qid": 20257872, "magnitude": 3, "destinationport": 53, "protocolid": 17, "sourceport": 50597, "identityip": "1.1.1.1", "sourceip": "1.1.1.1", "logsourceid": 71}, {"username": "None", "category": 8053, "starttime": 1548682800217, "destinationip": "1.1.1.1", "eventcount": 1, "qid": 20280296, "magnitude": 3, "destinationport": 443, "protocolid": 6, "sourceport": 49230, "identityip": "1.1.1.1", "sourceip": "1.1.1.1", "logsourceid": 71}]}
```



#### Lookup for a Value in Reference Set
Check if a value is listed in a specific reference set.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The name of the reference set to check a value.|True|String||
|Value|The value to check in a referenced set.|True|String||



##### JSON Results
```json
[{"last_seen": 1611149814345, "first_seen": 1611149814345, "source": "admin", "value": "192.168.xxx.xxx"}]
```



#### Lookup for a Value in Reference Tables
Check if a value is listed in a specific reference table. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The name of the reference table to check a value.|True|String||
|Value|The value to check in a referenced table.|True|String||



##### JSON Results
```json
[{"last_seen":1612806491507,"first_seen":1612806487352,"source":"reference data api","value":"value2","inner_key":"innerKey1","outer_key":"outerKey1"},{"last_seen":1612806491507,"first_seen":1612806487352,"source":"reference data api","value":"value2","inner_key":"innerKey2","outer_key":"outerKey2"}]
```



#### List Reference Maps of Sets
List reference maps of sets available in Qradar.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Fields To Return|Specify which fields should be returned by the action. If nothing is provided - return all available fields by default. Parameter accepts multiple values separated by comma.|False|String||
|Filter Condition|Specify a filter condition to return only specific elements, for example: element_type = ALN.|False|String||
|Number Of Elements To Return|Specify a maximum numbers of elements to return by the action.|True|String|25|



##### JSON Results
```json
[{"timeout_type":"UNKNOWN","number_of_elements":1,"creation_time":1611240976203,"name":"test","element_type":"ALN"},{"time_to_live":"0 years 2 mons 0 days 0 hours 0 mins 0.00 secs","timeout_type":"LAST_SEEN","number_of_elements":0,"creation_time":1440695697155,"value_label":"destinationip","name":"User-System Authentication or Usage","element_type":"IP","key_label":"username"},{"timeout_type":"UNKNOWN","number_of_elements":0,"creation_time":1399659402000,"name":"CorrelatedAttackMap","element_type":"ALN"}]
```



#### Similar Events Query
Execute a predefined AQL query to find events related to the specified Siemplify IP address, Hostname, or Username entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Time Delta In Minutes|Fetch events for the last X minutes. The parameter accepts numeric values for example, 10.|False|String|10|
|Events Limit To Fetch|Limit how many events the action can return, the parameter accepts numeric value, for example, 25.|True|String|25|
|Fields To Display|The fields to fetch from the event in addition to predefined ones, if not set - return predefined fields for the event.|False|String||
|Hostname Field Name|Field that represents Hostname Field of event|False|String||
|Source IP Address Field Name|Fields that represents Source IP Address Field of event|False|String||
|Destination IP Address Field Name|Fields that represents Destination IP Address Field of event|False|String||
|Username Field Name|Fields that represents Username Field of event|False|String||



##### JSON Results
```json
[{"Entity": "10.0.xx.xx", "EntityResult": [{"starttime": 1611130688377, "protocolid": "xx", "sourceip": "10.0.xx.xx", "logsourceid": "xx", "qid": "2825xxx", "sourceport": 0, "eventcount": 1, "magnitude": 7, "identityip": "0.0.xx.xx", "destinationip": "172.30.xx.xx", "destinationport": 0, "category": 16003, "username": "API_Auth"}, {"starttime": 1611130698343, "protocolid": "xx", "sourceip": "10.0.xx.xx", "logsourceid": "xx", "qid": "2825xxx", "sourceport": 0, "eventcount": 1, "magnitude": 7, "identityip": "0.0.xx.xx", "destinationip": "172.30.xx.xx", "destinationport": 0, "category": 16003, "username": "API_Auth"}]}]
```



#### Get Rule MITRE Coverage
Get MITRE details about rules in Qradar using the Use Case Manager application.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Rule Names|Specify a comma-separated list of rule names for which action should return MITRE details.|True|String||
|Create Insight|If enabled, action will create an insight containing information about MITRE coverage of the rules.|False|Boolean|true|



##### JSON Results
```json
[{"rulename":"Excessive Database Connections","id":"SYSTEM-xxxx","has_ibm_default":true,"last_updated":1591634177302,"mapping":{"Discovery":{"confidence":"medium","user_override":false,"enabled":true,"ibm_default":true,"id":"TAxxxx","techniques":{}},"Initial Access":{"confidence":"low","user_override":false,"enabled":true,"ibm_default":true,"id":"TAxxxx","techniques":{}}},"min-mitre-version":7},{"rulename":"4897fd3d-d623-4727-83a5-xxxxxxxxxx","id":"4897fd3d-d623-4727-83a5-xxxxxxxxxx","has_ibm_default":true,"last_updated":1607611408002,"mapping":{"Initial Access":{"confidence":"medium","user_override":false,"enabled":true,"ibm_default":true,"id":"TAxxxx","techniques":{"Spearphishing Link":{"confidence":"medium","enabled":true,"id":"T1xxxx","parentTechniqueName":"Phishing"},"Spearphishing Attachment":{"confidence":"medium","enabled":true,"id":"T1xxxx","parentTechniqueName":"Phishing"}}},"Credential Access":{"confidence":"low","user_override":false,"enabled":true,"ibm_default":true,"id":"TAxxxx","techniques":{}}},"min-mitre-version":7}]
```



#### Lookup for a Value in Reference Map
Check if a value is listed in a specific reference map. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The name of the reference map to check a value.|True|String||
|Value|The value to check in a referenced map.|True|String||



##### JSON Results
```json
[{"last_seen":1586154232667,"key":"1001","first_seen":1586154232667,"source":"reference data api","value":"jack"}]
```



#### Similar Flows Query
Execute a predefined AQL query to find flows related to the specified Siemplify IP address entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Time Delta In Minutes|Fetch flows for the last X minutes. The parameter accepts numeric values for example, 10.|False|String|10|
|Flows Limit To Fetch|Limit how many flows the action can return, parameter accepts numeric values for example, 10.|True|String|25|
|Fields To Display|The fields to fetch from the flow in addition to predefined ones, if not set - return predefined fields for the flow.|False|String||
|Source IP Address Field Name|Fields that represents Source IP Address Field of flow.|False|String||
|Destination IP Address Field Name|Fields that represents Destination IP Address Field of flow.|False|String||



##### JSON Results
```json
[{"Entity": "10.0.xx.xx", "EntityResult": [{"destinationflags": 27, "destinationpackets": 4.0, "sourcebytes": 902.0, "protocolid": "xx", "sourceip": "10.0.xx.xx", "destinationbytes": 381.0, "lastpackettime": 1611130664808, "sourceflags": 27, "sourcepackets": 6.0, "qid": "5325xxx", "flowtype": 0, "destinationip": "172.30.xx.xx", "firstpackettime": 1611130663789, "category": 18448}, {"destinationflags": 26, "destinationpackets": 20.0, "sourcebytes": 7238.0, "protocolid": "xx", "sourceip": "10.0.xx.xx", "destinationbytes": 34133.0, "lastpackettime": 1611130667352, "sourceflags": 26, "sourcepackets": 22.0, "qid": "5325xxx", "flowtype": 0, "destinationip": "172.30.xx.xx", "firstpackettime": 1611130664473, "category": 18448}, {"destinationflags": 27, "destinationpackets": 11.0, "sourcebytes": 903.0, "protocolid": "xx", "sourceip": "10.0.xx.xx", "destinationbytes": 799.0, "lastpackettime": 1611130662089, "sourceflags": 27, "sourcepackets": 6.0, "qid": "5325xxx", "flowtype": 0, "destinationip": "172.30.xx.xx", "firstpackettime": 1611130628768, "category": 18448}, {"destinationflags": 16, "destinationpackets": 1.0, "sourcebytes": 64.0, "protocolid": "xx", "sourceip": "10.0.xx.xx", "destinationbytes": 58.0, "lastpackettime": 1611130622755, "sourceflags": 17, "sourcepackets": 1.0, "qid": "5325xxx", "flowtype": 0, "destinationip": "172.30.xx.xx", "firstpackettime": 1611130598337, "category": 18448}, {"destinationflags": 27, "destinationpackets": 16.0, "sourcebytes": 2078.0, "protocolid": "xx", "sourceip": "10.0.xx.xx", "destinationbytes": 5250.0, "lastpackettime": 1611130659361, "sourceflags": 27, "sourcepackets": 16.0, "qid": "5325xxx", "flowtype": 0, "destinationip": "172.30.xx.xx", "firstpackettime": 1611130657293, "category": 18448}, {"destinationflags": 27, "destinationpackets": 4.0, "sourcebytes": 902.0, "protocolid": "xx", "sourceip": "10.0.xx.xx", "destinationbytes": 381.0, "lastpackettime": 1611130667602, "sourceflags": 27, "sourcepackets": 6.0, "qid": "5325xxx", "flowtype": 0, "destinationip": "172.30.xx.xx", "firstpackettime": 1611130666583, "category": 18448}]}]
```



#### Add Offense Note
Add a note to a Qradar offense.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Offense ID|Offense ID to add a note to.|True|String||
|Note Text|Note text to add to offense.|True|String||






## Jobs

#### SyncCloseOffenses
Closes related Qradar offenses for closed Siemplify alerts.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|https://x.x.x.x|
|API Token|True|Password|*****|
|API Version|False|String||
|Days Backwards|False|Integer|1|

#### Dummy Job




## Connectors
#### Qradar Baseline Offenses Connector
Qradar Baseline Offenses connector used to fetch offenses and create Chronicle SOAR alerts based on the Qradar offenses names. Connector will create a single SOAR alert per Qradar offense, and will not try to create additional SOAR alerts with new events from Qradar. Connector uses SOAR dynamic list, but by default if no whitelist rules are set, it will fetchingest all offenses returned from the Qradar API offenses. Connector requires Qradar API version 10.1 or higher.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Describes the name of the field where the product name is stored.|True|String|deviceProduct|
|EventClassId|Describes the name of the field where the event name is stored|False|String|EventName|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is default environment|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.|False|String|.*|
|API Root|The API server address.|True|String|https://x.x.x.x:port|
|API Token|The API authentication token.|True|Password|*****|
|API Version|The Qradar API version to be used, the Connector supports API version starting from 10.1.|True|String|10.1|
|Total limit of events per offense|Specify how many events per Qradar offense should be ingested in total by connector, after reaching that limit  new events will not be ingested for the offense.|True|Integer|100|
|Connector Events Page Size|The size of the page that connector will use to process events in batches.|True|Integer|100|
|Max Offenses per Cycle|Max offenses to process per connector run. Note: it’s not recommended to put a value lower than 10.|True|Integer|10|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|300|
|Max Days Backwards|Number of days before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Integer|1|
|Offenses Padding Period|Time frame in minutes to fetch offenses in minutes.|True|Integer|60|
|Events Padding Period|Time frame in days to fetch events data.|True|Integer|1|
|Events Limit per Qradar Offence Rule|Specify an optional limit for how many events should be ingested per single rule in Qradar offense, no new events will be ingested to the offense for the related Qradar rule once this limit is reached. Limit cant be bigger than 'Total limit of events per offense'.|False|Integer||
|Custom Fields|Custom fields that configured by the user at the QRadar, comma separated, e.g: Field A,Field B|False|String||
|Domain Filter|Specify Qradar domains from which offenses should be ingested. If no values are provided, the connector will ingest offenses from all domains. Parameter accepts multiple values as a comma separated string.|False|String||
|Magnitude Filter|Specify an offense magnitude to ingest, offenses with the magnitude equal or bigger than provided will be ingested to Siemplify.|False|Integer||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|What Value to use for the Name Field of Siemplify Alert?|Specify what format to follow to generate names for the alerts created by the connector. Possible values are: custom_alert_name or offense_description.|False|String|custom_alert_name|
|Use dynamic list as a blocklist|If enabled, dynamic lists will be used as a blocklist. If the checkbox is not enabled and no allow rules are set, the connector will fetch all offenses returned from the Qradar API.|False|Boolean|false|
|Disable Overflow|If enabled, connector overflow mechanism will not be checked for the created alerts - “overflow” alerts will not be created, connector will try to fetch all offenses returned from the Qradar.|False|Boolean|false|
|Qradar Offense Rules Re-Sync Timer|Specify in minutes how often connector should re-sync Qradar offense rules list. If empty value or 0 is specified, connector will do re-sync every run.|False|Integer|10|
|Debug Logging|If enabled, connector will write detailed messages of its execution to the log file.|False|Boolean|false|
|Create SOAR alerts for offenses with 0 events|If enabled, connector will create a SOAR alert using the Qradar offense data for both alert and event for offenses that were fetched with no events.|False|Boolean|false|
|Offenses Creation Timer (minutes)|Specify the amount of time in minutes to pass before the connector will try to fetch events data for the newly created Qradar offense. If the connector failed to get the events after the configured amount of time have passed, and if the "Create SOAR alerts if failed to get events for it?" parameter is enabled, the connector will use the fallback to create SOAR alert and event from the same Qradar offense data.|False|Integer|5|


#### Qradar Offenses Connector
Qradar offenses connector used to fetch offenses and create Chronicle SOAR (CSOAR) alerts based on the Qradar offenses themselves, in opposite how other integration’s connectors do it based on the Qradar rule names. Connector has a limit of how many events in total it will fetch per Qradar offense, after reaching that limit new events will not be ingested. Connector uses CSOAR dynamic list, but by default if no whitelist rules are set, it will fetch all offenses returned from the Qradar API. Connector requires Qradar API version 10.1 or higher. Connector can be considered as an easier to configure and use version that can be utilized if there is no need to track and ingest all Qradar offense events and ingest them to CSOAR (as integration  correlation connectors do).

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Describes the name of the field where the product name is stored.|True|String|deviceProduct|
|EventClassId|Describes the name of the field where the event name is stored|False|String|EventName|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is default environment|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.|False|String|.*|
|API Root|The API server address.|True|String|https://x.x.x.x:port|
|API Token|The API authentication token.|True|Password|*****|
|API Version|The Qradar API version to be used, the Connector supports API version starting from 10.1.|True|String|10.1|
|Total limit of events per offense|Specify how many events per Qradar offense should be ingested in total by connector, after reaching that limit  new events will not be ingested for the offense.|True|Integer|100|
|Connector Events Page Size|The size of the page that connector will use to process events in batches.|True|Integer|100|
|Max Offenses per Cycle|Max offenses to process per connector run.|True|Integer|10|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|300|
|Max Days Backwards|Number of days before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Offenses Padding Period|Time frame in minutes to fetch offenses in minutes.|True|Integer|60|
|Events Padding Period|Time frame in days to fetch events data.|True|Integer|1|
|Events Limit per Qradar Offence Rule|Specify an optional limit for how many events should be ingested per single rule in Qradar offense, no new events will be ingested to the offense for the related Qradar rule once this limit is reached. Limit cant be bigger than 'Total limit of events per offense'.|False|Integer||
|Custom Fields|Custom fields that configured by the user at the QRadar, comma separated, e.g: Field A,Field B|False|String||
|Domain Filter|Specify Qradar domains from which offenses should be ingested. If no values are provided, the connector will ingest offenses from all domains. Parameter accepts multiple values as a comma separated string.|False|String||
|Magnitude Filter|Specify an offense magnitude to ingest, offenses with the magnitude equal or bigger than provided will be ingested to Siemplify.|False|Integer||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|What Value to use for the Name Field of Siemplify Alert?|Specify what format to follow to generate names for the alerts created by the connector. Possible values are: custom_alert_name or offense_description.|False|String|custom_alert_name|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist. If the checkbox is not enabled and no whitelist rules are set, the connector will fetch all offenses returned from the Qradar API.|False|Boolean|false|
|Disable Overflow|If enabled, connector overflow mechanism will not be checked for the created alerts - “overflow” alerts will not be created, connector will try to fetch all offenses returned from the Qradar.|False|Boolean|false|
|Qradar Offense Rules Re-Sync Timer|Specify in minutes how often connector should re-sync Qradar offense rules list. If empty value or 0 is specified, connector will do re-sync every run.|False|Integer|10|
|Debug Logging|If enabled, connector will write detailed messages of its execution to the log file.|False|Boolean|false|


#### Qradar Correlation Events Connector V2
Fetches Qradar offenses and forms Chronicle SOAR (CSOAR) alerts for each Qradar rule added to dynamic list in CSOAR. Connector fetches only the offenses for rules that are added to CSOAR dynamic list. Connector requires minimum Qradar API version 10.1. Connector creates CSOAR alerts based on the rule name of Qradar offense, not the offense name.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Describes the name of the field where the product name is stored.|True|String|deviceProduct|
|EventClassId|Describes the name of the field where the event name is stored|False|String|EventName|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|300|
|API Root|Qradar Server address.|True|String|https://x.x.x.x:port|
|API Token|The API authentication token.|True|Password|*****|
|API Version|The Qradar API version to be used, the Connector supports API version starting from 10.1.|True|String|10.1|
|Connector Events Page Size|The size of the page that connector will use to process events in batches.|True|Integer|100|
|Max Offenses per Cycle|Max offenses to process per connector run.|True|Integer|5|
|Events Limit per Siemplify Alert|Max number of events to fetch per Siemplify Alert per Cycle. Can be increased to make connector run faster, if for the specified offense padding period, large numbers of events are constantly returned.|True|Integer|25|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|24|
|Offenses Padding Period|Time frame in minutes to fetch offenses in minutes.|True|Integer|60|
|Events Padding Period|Time frame in days to fetch events data.|True|Integer|1|
|Custom Fields|Custom fields that configured by the user at the QRadar, comma separated, e.g: FieldA,Field B|False|String||
|What Value to use for the Name Field of Siemplify Alert?|Specify what format to follow to generate names for the alerts created by the connector. Possible values are: custom_rule or offense_description.|False|String|custom_rule|
|What Value to use for the Rule Generator Field of Siemplify Alert?|Specify what format to follow to fill the rule_generator field for the alerts created by the connector. Possible values are: custom_rule or offense_description.|False|String|custom_rule|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is default environment|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.|False|String|.*|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Domain Filter|Specify qradar domains from which offenses should be ingested. If no values are provided, the connector will ingest offenses from all domains. Parameter accepts multiple values as a comma separated string.|False|String||
|Events Limit per Qradar Offense Rule|Specify a limit for how many events should be ingested per single rule in Qradar offense, no new events will be ingested to the offense for the related Qradar rule once this limit is reached. Example: 100|False|Integer|100|
|Events Limit for Connector to Query in One Connector Run|Specify a limit for how many events for a single offense connector should query from Qradar in one connector execution. Example: 100. Note that the value specified in the parameter can't be less than the value specified in "Events Limit per Qradar Offense Rule" parameter. Additionally, because of how connector fetches events, events that will be "older" and outside the limit will not be fetched to Siemplify, but connector will fetch newest events until the limit specified in "Events Limit per Qradar Offense Rule" parameter is reached.|False|Integer||
|Disable Overflow|If enabled, connector overflow mechanism will not be checked for the created alerts - "overflow" alerts will not be created, connector will try to fetch all offenses returned from the Qradar.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Qradar Offense Rules Re-Sync Timer|Specify in minutes how often connector should re-sync Qradar offense rules list. If empty value or 0 is specified, connector will do re-sync every run.|False|Integer|10|
|Debug Logging|If enabled, connector will write detailed messages of its execution to the log file.|False|Boolean|false|


##### Allowlist
| |
|-|
|Local: SSH or Telnet Detected on Non-Standard Port|
|Multiple Login Failures from the Same Source|




