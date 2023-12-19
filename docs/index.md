---
icon: home
label: Home
---

![](/static/hero.webp)

# Welcome to the Docs!

The SA-SentinelOneDevices Add-on allows Splunk Enterprise Security admins to use [SentinelOne <small>:icon-link-external:</small>][so]{ target="blank" } asset data with the Asset Database. This documentation will cover the components used in the add-on and advanced configurations. 

!!!danger Important
This Supporting add-on is only intended to work with [Splunk Enterprise Security <small>:icon-link-external:</small>](https://splunkbase.splunk.com/app/263){ target="blank" } deployments.
!!!

> __*Disclaimer*__
> 
> *This Splunk Supporting Add-on is __not__ affiliated with [__SentinelOne, Inc.__ <small>:icon-link-external:</small>][so]{ target="blank" } and is not sponsored or sanctioned by the SentinelOne team. Please visit [https://www.sentinelone.com/ <small>:icon-link-external:</small>][so]{ target="blank" } for more information about SentinelOne.*

## Assumptions

This documentation assumes the following:

1. You have a working Splunk Enterprise Security environment. __This add-on is not intended to work without Splunk Enterprise Security.__
2. You already have SentinelOne device data ingested using the [SentinelOne App For Splunk <small>:icon-link-external:</small>](https://splunkbase.splunk.com/app/5433){ target="blank" }.
3. Familiarity with setting up a new Asset source in Splunk Enterprise Security.

## About

Info | Description
------|----------
SA-SentinelOneDevices | 1.0.2 - [Splunkbase <small>:icon-link-external:</small>](https://splunkbase.splunk.com/app/6612/){ target="blank" } 
Splunk Enterprise Security Version <small>(Required)</small> | [7.x \| 6.x <small>:icon-link-external:</small>](https://splunkbase.splunk.com/app/263){ target="blank" }
SentinelOne App For Splunk <small>(Required)</small> | [5.1.x <small>:icon-link-external:</small>](https://splunkbase.splunk.com/app/5433){ target="blank" }
Add-on has a web UI | No, this add-on does not contain views.

[so]: https://www.sentinelone.com/
