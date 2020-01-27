# Event ID 4659: A handle to an object was requested with intent to delete

## Description

A handle to an object was requested with intent to delete

## Event Log Illustration & Event XML



## Data Dictionary

|	Standard Name	|	Field Name	|	Type	|	Description	|	Sample Value	|
|	----------------	|	----------------	|	----------------	|	----------------	|	----------------	|
|	user_sid	|	SubjectUserSid	|	string	|	SID of account to which special privileges were assigned	|	S-1-5-21-3457937927-2839227994-823803824-1104		|
|	user_name	|	SubjectUserName	|	string	|	the name of the account to which special privileges were assigned	|	dadmin		|
|	user_domain	|	SubjectDomainName	|	string	|	subject’s domain or computer name	|	CONTOSO		|
|	user_logon_id	|	SubjectLogonId	|	integer	|	hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID	|	0x671101		|
|	object_name	|	ObjectName	|	string	|	string|the name of the object that was accessed during the operation	|	-		|
|	object_server		|	ObjectServer	|	string	|	Contains the name of the Windows subsystem calling the routine	|	-		|
|	object_type		|	ObjectType	|	string	|	The type of an object that was accessed during the operation	|	-		|
|	object_handle_id		|	HandleId	|	integer	|	hexadecimal value of a handle to Object Name. This field can help you correlate this event with other events that might contain the same Handle ID	|	0x0		|
|	object_access_mask		|	AccessMask	|	string	|	The desired access mask. This mask depends on Object Server and Object Type parameters values. The value of this parameter is in decimal format. There is no detailed information about this parameter in this document. If Desired Access is not presented, then this parameter will have “0” value.	|	-		|
|	transaction_guid		|	TransactionId	|	string	|	unique GUID of the transaction. This field can help you correlate this event with other events that might contain the same Transaction ID	|	-		|
|	object_access_list		|	AccessList	|	string	|	the list of user privileges which were requested	|	-		|
