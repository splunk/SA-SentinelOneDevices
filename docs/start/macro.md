---
order: -3
label: Update Index
icon: command-palette
---

# Update Splunk Index

!!!danger [Danger, Will Robinson <small>:icon-link-external:</small>](https://cultural-phenomenons.fandom.com/wiki/Danger,_Will_Robinson){ target="blank" }
Failure to update the index to the correct setting will cause no devices to be available in Splunk Enterprise Security.
!!!

The index definition is set by a search macro. 

Macro | Default | Description
----- | ------- | -----------
sa_sentinelone_index | index=sentinelone | Index definition for SentinelOne index.

!!!
Update the index definition to the correct index that contains the `sentinelone:channel:agents` sourcetype.
!!!

## How to update

==- :icon-star-fill: Use Splunk Enterprise Security's Settings <small>(Recommended)</small>
1. <small>(In Splunk Enterprise Security)</small> Navigate to Configure > General > General Settings.
2. From the "App" dropdown select `SA-SentinelOneDevices`.
3. Update the SA-SentinelOneDevices Index definition and click "Save."
==- Update Search Macro Manually
1. Navigate to Settings > Advanced Search > Search Macros.
2. From the "App" dropdown choose `SA-SentinelOneDevices`.
3. Set the "Owner" dropdown to `any`.
4. Click the macro named `sa_sentinelone_index` to update the index definition.
===