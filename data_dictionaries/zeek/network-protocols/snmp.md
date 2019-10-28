# SNMP Log

## Description

## Event JSON

```json
```

## Data Dictionary

|	        Standard Name       	|            Field Name             |       	    Type            	|   	    Description          	|	     Sample Value           	|
|	-------------------------------	|	-------------------------------	|	-------------------------------	|	-------------------------------	|	-------------------------------	|
|#TODO:NewFieldName|@stream|string||
|#TODO:NewFieldName|ts|date_time||
|#TODO:NewFieldName|id.orig_h|ip||
|#TODO:NewFieldName|id.orig_p|integer||
|#TODO:NewFieldName|id.resp_h|ip||
|#TODO:NewFieldName|id.resp_p|integer||
|#TODO:NewFieldName|uid|string|Unique ID for the connection.|
|#TODO:NewFieldName|duration|float|The amount of time between the first packet beloning to the SNMP session and the latest one seen.|
|#TODO:NewFieldName|community|string|The community string of the first SNMP packet associated with the session. This is used as part of SNMP’s (v1 and v2c) administrative/security framework. See RFC 1157 or RFC 1901.|
|#TODO:NewFieldName|display_string|string|A system description of the SNMP responder endpoint.|VMware ESXi 5.5.0 build-4722766 VMware, Inc. x86_64;Hardware: Intel64 Family 6 Model 45 Stepping 7 AT/AT COMPATIBLE - Software: Windows Version 6.3 (Build 9600 Multiprocessor Free)
|#TODO:NewFieldName|get_bulk_requests|integer|The number of variable bindings in GetBulkRequest PDUs seen for the session.|
|#TODO:NewFieldName|get_requests|integer|The number of variable bindings in GetRequest/GetNextRequest PDUs seen for the session.|
|#TODO:NewFieldName|get_responses|integer|The number of variable bindings in GetResponse/Response PDUs seen for the session.|
|#TODO:NewFieldName|set_requests|integer|The number of variable bindings in SetRequest PDUs seen for the session.|
|#TODO:NewFieldName|up_since|date_time|The time at which the SNMP responder endpoint claims it’s been up since.|
|#TODO:NewFieldName|version|string|The version of SNMP being used.|1;2c;3