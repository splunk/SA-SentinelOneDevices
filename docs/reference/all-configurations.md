---
hide:
    - toc
---
# All Configurations

Below is a table that list all configuration for this add-on.

Name | Type | Web Location | CLI Location\* | Description
---- | ---- | ------------ | ------------- | -----------
SentinelOne Devices Lookup - Gen | Saved Search | Settings > Searches reports, and alerts | savedsearches.conf | Populates the lookup file `sentinelone_devices`.
SentinelOne Devices Lookup - Cleanup | Saved Search | Settings > Searches reports, and alerts | savedsearches.conf | removes old entries from kvstore lookup: `sentinelone_devices`.
sentinelone_devices | lookup | Settings > Lookups > Lookup definitions | transforms.conf | Lookup definition for the KVstore collection `sentinelone_devices_collection`.
sentinelone_devices_collection | KVStore collection | n/a\*\* | collections.conf | KVstore configuration.
sa_sentinelone_index | Search macro | Settings > Advanced Search > Search Macros | macros.conf | Index definition for the sentinelone index that contains the sourcetype `sentinelone:channel:agents`.
sa_sentinelone_retention | Search macro | Settings > Advanced Search > Search Macros | macros.conf | The amount of time for the device not being updated before it is removed from the lookup. `default "-2d"`
identity_manager://sentinelone_devices | Asset lookup configuration | Enterprise Security > Configure > Data Enrichment > Asset and Identity Management > Asset Lookups | inputs.conf | Asset configuration lookup to load SentinelOne devices into the asset database.

> \*CLI locations are relative to `../default`. Any update to CLI configuration files should be done in the local directory.

!!! note ""
    **If you have the [Splunk App for Lookup File Editing](https://splunkbase.splunk.com/app/263), the KVStore collection `sentinelone_devices_collection` is viewable within the Web interface.
