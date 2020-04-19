---
title: Event ID 21 - WmiEvent (WmiEventConsumerToFilter activity detected)
description: When a consumer binds to a filter, this event logs the consumer name and filter path.
log.type: sysmon
sysmon.version: 9.01
sysmon.rule: WmiEvent
author: Roberto Rodriguez (@Cyb3rWard0g)
date: 04/26/2019
---

# Event ID 21: WmiEvent (WmiEventConsumerToFilter activity detected)

## Description
When a consumer binds to a filter, this event logs the consumer name and filter path.[Sysmon Source](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-21-wmievent-wmieventconsumertofilter-activity-detected)

## Event Log Illustration

<img src="https://github.com/Cyb3rWard0g/OSSEM/blob/master/resources/images/event-21.png" alt="Event 21 illustration" width="625" height="625">

## Event XML

```
<Event xmlns="http://schemas.microsoft.com/win/2004/08/events/event">
  <System>
    <Provider Name="Microsoft-Windows-Sysmon" Guid="{5770385f-c22a-43e0-bf4c-06f5698ffbd9}" /> 
    <EventID>21</EventID> 
    <Version>3</Version> 
    <Level>4</Level> 
    <Task>21</Task> 
    <Opcode>0</Opcode> 
    <Keywords>0x8000000000000000</Keywords> 
    <TimeCreated SystemTime="2019-04-27T01:04:06.885559700Z" /> 
    <EventRecordID>3633050</EventRecordID> 
    <Correlation /> 
    <Execution ProcessID="1432" ThreadID="5672" /> 
    <Channel>Microsoft-Windows-Sysmon/Operational</Channel> 
    <Computer>WARDOG.RIVENDELL.local</Computer> 
    <Security UserID="S-1-5-18" /> 
  </System>
  <EventData>
    <Data Name="RuleName" /> 
    <Data Name="EventType">WmiBindingEvent</Data> 
    <Data Name="UtcTime">2019-04-27 01:04:06.885</Data> 
    <Data Name="Operation">Created</Data> 
    <Data Name="User">RIVENDELL\cbrown</Data> 
    <Data Name="Consumer">"CommandLineEventConsumer.Name=\"Updater\""</Data> 
    <Data Name="Filter">"__EventFilter.Name=\"Updater\""</Data> 
  </EventData>
</Event>
```

## Data Dictionary

|	Standard Name	| Field Name |	Type	|	Description	|	Sample Value	|
|	----------------	|	----------------	|	----------------	|	----------------	|	----------------	|
| tag               | RuleName  | string | custom tag mapped to event. i.e ATT&CK technique ID | T1114                                     |
| event_type        | EventType | string | wmievent type                                       | WmiBindingEvent                           |
| @timestamp        | UtcTime   | date   | Time in UTC when event was created                  | 2018-09-12 00:47:16.997                   |
| wmi_operation     | Operation | string | wmievent filter operation                           | Created                                   |
| user_name         | User      | string | user that created the wmi filter                    | DESKTOP-LFD11QP\pedro                     |
| wmi_consumer_path | Consumer  | string | Consumer created to bind                            | CommandLineEventConsumer.Name=\"Updater\" |
| wmi_filter_path   | Filter    | string | Filter created to bind                              | __EventFilter.Name=\"Updater\"            |
