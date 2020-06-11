# Event ID 4818: Proposed Central Access Policy does not grant the same access permissions as the current Central Access Policy.

## Description
This event generates when Dynamic Access Control Proposed Central Access Policy is enabled and access was not granted by Proposed Central Access Policy.

## Data Dictionary
|Standard Name|Field Name|Type|Description|Sample Value|
|---|---|---|---|---|
|user_sid|SubjectUserSid|SID|SID of account that made an access request.|`S-1-5-21-3457937927-2839227994-823803824-2104`|
|user_name|SubjectUserName|UnicodeString|the name of the account that made an access request.|`Auditor`|
|user_domain|SubjectDomainName|UnicodeString|subject's domain or computer name.|`CONTOSO`|
|user_logon_id|SubjectLogonId|HexInt64|hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID, for example, "4624: An account was successfully logged on."|`0x1e5f21`|
|object_server|ObjectServer|UnicodeString|has "Security" value for this event.|`Security`|
|object_type|ObjectType|UnicodeString|The type of an object that was accessed during the operation. Always "File" for this event.|`File`|
|file_path|ObjectName|UnicodeString|full path and name of the file or folder for which access was requested.|`C:\Finance Documents\desktop.ini`|
|object_handle_id|HandleId|Pointer|hexadecimal value of a handle to Object Name.|`0xc64`|
|process_id|ProcessId|Pointer|hexadecimal Process ID of the process through which the access was requested.|`0x4`|
|process_path|ProcessName|UnicodeString|full path and the name of the executable for the process.|`None`|
|access_reason|AccessReason|UnicodeString|the list of access check results for Current Access Policy.|`%%1538: %%1801 D:(A;ID;0x1200a9;;;BU) %%1541: %%1801 D:(A;ID;0x1200a9;;;BU) %%4416: %%1801 D:(A;ID;0x1200a9;;;BU) %%4419: %%1801 D:(A;ID;0x1200a9;;;BU) %%4423: %%1801 D:(A;ID;0x1200a9;;;BU)`|
|staging_reason|StagingReason|UnicodeString|the list of access check results for Proposed Central Access Policy.|`%%1538: %%1814Finance Documents Rule %%1541: %%1814Finance Documents Rule %%4416: %%1814Finance Documents Rule %%4419: %%1814Finance Documents Rule %%4423: %%1814Finance Documents Rule`|

## References
* [MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/public/windows/security/threat-protection/auditing/event-4818.md)
* [MS Security Auditing Category - Object Access](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings#object-access)
* [MS Security Auditing Sub-category - Audit Central Access Policy Staging](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/master/windows/security/threat-protection/auditing/audit-central-access-policy-staging.md)

## Tags
* etw_level_Informational
* etw_task_task_0
* Object Access
* Audit Central Access Policy Staging