# Event ID 4728: A member was added to a security-enabled global group.

## Description

See event _[4732](event-4732.md): A member was added to a security-enabled local group._ Event 4728 is the same, but it is generated for a **global** security group instead of a **local** security group. All event fields, XML, and recommendations are the same. The type of group is the only difference.

  > [!IMPORTANT]
  > Event 4728(S) generates only for domain groups, so the Local sections in event [4732](event-4732.md) do not apply.

[MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/b7c0643659189d384c8fa4b234256bdaef176b02/windows/security/threat-protection/auditing/audit-security-group-management.md#L67)

## Event Log Illustration & Event XML

[MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/master/windows/security/threat-protection/auditing/event-4732.md)

## Data Dictionary

|	Standard Name	|	Field Name	|	Type	|	Description	|	Sample Value	|
|	----------------	|	----------------	|	----------------	|	----------------	|	----------------	|
|	target_user_name	|	MemberName	|	string	|	distinguished name of account that was added to the group. For example: “CN=Auditor,CN=Users,DC=contoso,DC=local”. For local groups this field typically has “-“ value, even if new member is a domain account.	|	CN=eadmin,CN=Users,DC=contoso,DC=local	|
|	target_user_sid	|	MemberSid	|	string	|	SID of account that was added to the group.	|	S-1-5-21-3457937927-2839227994-823803824-500	|
|	group_name	|	TargetUserName	|	string	|	the name of the group to which new member was added.	|	AccountOperators	|
|	group_domain	|	TargetDomainName	|	string	|	domain or computer name of the group to which the new member was added.	|	CONTOSO	|
|	group_sid	|	TargetSid	|	string	|	SID of the group to which new member was added.	|	S-1-5-21-3457937927-2839227994-823803824-6605	|
|	user_sid	|	SubjectUserSid	|	string	|	SID of account that requested the “add member to the group” operation.	|	S-1-5-21-3457937927-2839227994-823803824-1104	|
|	user_name	|	SubjectUserName	|	string	|	the name of the account that requested the “add member to the group” operation.	|	dadmin	|
|	user_domain	|	SubjectDomainName	|	string	|	subject’s domain or computer name.	|	CONTOSO	|
|	user_logon_id	|	SubjectLogonId	|	integer	|	hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID, for example, “4624: An account was successfully logged on.”	|	0x3031e	|
|	user_privilege_list	|	PrivilegeList	|	string	|	the list of user privileges which were used during the operation, for example, SeBackupPrivilege. This parameter might not be captured in the event, and in that case appears as “-”.	|	-	|