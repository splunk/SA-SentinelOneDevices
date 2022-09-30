---
hide:
    - toc
---

# Asset Database Mapping

The following table describes how this add-on maps to the Asset Database.

> reference [Format an asset or identity in Splunk ES](https://docs.splunk.com/Documentation/ES/latest/Admin/Formatassetoridentitylist#Asset_lookup_header)

ES Asset lookup field | [SentinelOne App For Splunk](https://splunkbase.splunk.com/app/5433) | Example value | Multivalue allowed
--- | --- | --- | ---
ip | `networkInterfaces{}.inet{}` | 10.15.23.8 | true
mac | `networkInterfaces{}.physical` | 61:se:e3:1s:7r:38 | true
nt_host | `computerName` | dev-server01 | false
dns | `nt_host` + `domain` | dev-server01.example.com | true
owner | `accountName` | demo_team | false
priority | see [Configure Priority](/configure/priority) | medium | false
lat | from `iplocation` of `externalIp` | 40.76073 | false
long | from `iplocation` of `externalIp` | -111.89096 | false
city | from `iplocation` of `externalIp` | Salt Lake City | false
country | from `iplocation` of `externalIp` | United States | false
bunit | `groupName` + `siteName` | computer,finance | true
category | see [Category field reference](../category) | see [Category field reference](../category) | true
pci_domain | n/a | `not mapped` | n/a
is_expected | set to true if priority="critical" | true | false
should_timesync | n/a | `not mapped` | n/a
should_update | n/a | `not mapped` | n/a
requires_av | n/a | `not mapped` | n/a
cim_entity_zone | n/a | `not mapped` | n/a
