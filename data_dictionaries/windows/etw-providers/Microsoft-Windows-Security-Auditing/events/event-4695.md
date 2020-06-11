# Event ID 4695: Unprotection of auditable protected data was attempted.

## Description
This event generates if DPAPI CryptUnprotectData() function was used to unprotect "auditable" data that was encrypted using CryptProtectData() function with CRYPTPROTECT_AUDIT flag (dwFlags) enabled.

## Data Dictionary
|Standard Name|Field Name|Type|Description|Sample Value|
|---|---|---|---|---|
|user_sid|SubjectUserSid|SID|SID of account that requested the "recover" operation.|`S-1-5-21-3457937927-2839227994-823803824-1104`|
|user_name|SubjectUserName|UnicodeString|the name of the account that requested the "recover" operation.|`dadmin`|
|user_domain|SubjectDomainName|UnicodeString|subject's domain or computer name.|`CONTOSO`|
|user_logon_id|SubjectLogonId|HexInt64|hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID, for example, 4624 An account was successfully logged on.|`0x30d7c`|
|TBD|DataDescription|UnicodeString|-|`71352374-45c5-4fb6-829b-9ff951a9e7aa`|
|TBD|MasterKeyId|UnicodeString|-|`UI1`|
|TBD|ProtectedDataFlags|HexInt32|-|`0x10`|
|TBD|CryptoAlgorithms|UnicodeString|Cryptographic Algorithms of the protection|`AES-256,SHA2-512`|
|TBD|FailureReason|HexInt32|-|`0x0`|

## References
* [MS Source](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/event-4695)
* [MS Security Auditing Category - Detailed Tracking](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings#detailed-tracking)
* [MS Security Auditing Sub-category - Audit DPAPI Activity](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/audit-dpapi-activity)

## Tags
* etw_level_Informational
* etw_task_task_0
* Detailed Tracking
* DPAPI Activity