# Event ID 4672: Special privileges assigned to new logon

## Description
This event generates for new account logons if any of the following sensitive privileges are assigned to the new logon session:

## Data Dictionary
|Standard Name|Field Name|Type|Description|Sample Value|
|---|---|---|---|---|
|user_sid|SubjectUserSid|SID|SID of account to which special privileges were assigned|`S-1-5-21-3457937927-2839227994-823803824-1104`|
|user_name|SubjectUserName|UnicodeString|the name of the account to which special privileges were assigned|`dadmin`|
|user_domain|SubjectDomainName|UnicodeString|subject's domain or computer name|`CONTOSO`|
|user_logon_id|SubjectLogonId|HexInt64|hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID|`0x671101`|
|user_privilege_list|PrivilegeList|UnicodeString|the list of sensitive privileges, assigned to the new logon.|`SeTcbPrivilege SeSecurityPrivilege SeTakeOwnershipPrivilege SeLoadDriverPrivilege SeBackupPrivilege SeRestorePrivilege SeDebugPrivilege SeSystemEnvironmentPrivilege SeEnableDelegationPrivilege SeImpersonatePrivilege`|

## References
* [MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/master/windows/security/threat-protection/auditing/event-4672.md)
* [MS Security Auditing Category - Logon/Logoff](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings#logonlogoff)
* [MS Security Auditing Sub-category - Audit Special Logon](https://github.com/MicrosoftDocs/windows-itpro-docs/tree/master/windows/security/threat-protection/auditing/audit-special-logon.md)

## Tags
* etw_level_Informational
* etw_task_task_0
* Logon/Logoff
* Audit Special Logon