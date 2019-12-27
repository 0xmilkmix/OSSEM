# Event ID 4611: A trusted logon process has been registered with the Local Security Authority.

## Description

This event indicates that a logon process has registered with the Local Security Authority (LSA). Also, logon requests will now be accepted from this source.

At the technical level, the event does not come from the registration of a trusted logon process, but from a confirmation that the process is a trusted logon process. If it is a trusted logon process, the event generates.

A logon process is a trusted part of the operating system that handles the overall logon function for different logon methods (network, interactive, etc.).

You typically see these events during operating system startup or user logon and authentication actions

## Event Log Illustration & Event XML

[MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/master/windows/security/threat-protection/auditing/event-4611.md)

## Data Dictionary

|Standard Name|Field Name|Type|Description|Sample Value|
|---|---|---|---|---|
|user_sid|SubjectUserSid|string|SID of account that registered the trusted logon process.|S-1-5-18|
|user_name|SubjectUserName|string|the name of the account that registered the trusted logon process.|DC01$|
|user_domain|SubjectDomainName|string|subject's domain or computer name.|CONTOSO|
|user_logon_id|SubjectLogonId|integer|hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID, for example, "4624: An account was successfully logged on."|0x3e7|
|logon_process_name|LogonProcessName|string|the name of registered logon process.|Winlogon|

## Reference

[MS SOURCE](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/public/windows/security/threat-protection/auditing/event-4611.md)