# Qradar Correlation Events Connector V2
Fetches Qradar offenses and forms Chronicle SOAR (CSOAR) alerts for each Qradar rule added to dynamic list in CSOAR. Connector fetches only the offenses for rules that are added to CSOAR dynamic list. Connector requires minimum Qradar API version 10.1. Connector creates CSOAR alerts based on the rule name of Qradar offense, not the offense name.


Integration: QRadar

Integration Version: 60.0

Device Product Field: deviceProduct

Event Name Field: EventName
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|What Value to use for the Rule Generator Field of Siemplify Alert?|Specify what format to follow to fill the rule_generator field for the alerts created by the connector. Possible values are: custom_rule or offense_description.|False|custom_rule|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is default environment|False||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.|False|.*|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Domain Filter|Specify qradar domains from which offenses should be ingested. If no values are provided, the connector will ingest offenses from all domains. Parameter accepts multiple values as a comma separated string.|False||
|Events Limit per Qradar Offense Rule|Specify a limit for how many events should be ingested per single rule in Qradar offense, no new events will be ingested to the offense for the related Qradar rule once this limit is reached. Example: 100|False|100|
|Events Limit for Connector to Query in One Connector Run|Specify a limit for how many events for a single offense connector should query from Qradar in one connector execution. Example: 100. Note that the value specified in the parameter can't be less than the value specified in "Events Limit per Qradar Offense Rule" parameter. Additionally, because of how connector fetches events, events that will be "older" and outside the limit will not be fetched to Siemplify, but connector will fetch newest events until the limit specified in "Events Limit per Qradar Offense Rule" parameter is reached.|False||
|Disable Overflow|If enabled, connector overflow mechanism will not be checked for the created alerts - "overflow" alerts will not be created, connector will try to fetch all offenses returned from the Qradar.|False|false|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|300|
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False||
|Qradar Offense Rules Re-Sync Timer|Specify in minutes how often connector should re-sync Qradar offense rules list. If empty value or 0 is specified, connector will do re-sync every run.|False|10|
|Debug Logging|If enabled, connector will write detailed messages of its execution to the log file.|False|false|
|API Root|Qradar Server address.|True|https://172.30.3.10|
|API Token|The API authentication token.|True|***************|
|API Version|The Qradar API version to be used, the Connector supports API version starting from 10.1.|True|10.1|
|Connector Events Page Size|The size of the page that connector will use to process events in batches.|True|100|
|Max Offenses per Cycle|Max offenses to process per connector run.|True|5|
|Events Limit per Siemplify Alert|Max number of events to fetch per Siemplify Alert per Cycle. Can be increased to make connector run faster, if for the specified offense padding period, large numbers of events are constantly returned.|True|25|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|24|
|Offenses Padding Period|Time frame in minutes to fetch offenses in minutes.|True|60|
|Events Padding Period|Time frame in days to fetch events data.|True|1|
|Custom Fields|Custom fields that configured by the user at the QRadar, comma separated, e.g: FieldA,Field B|False|kmproperty|
|What Value to use for the Name Field of Siemplify Alert?|Specify what format to follow to generate names for the alerts created by the connector. Possible values are: custom_rule or offense_description.|False|custom_rule|

