# Update Cleanup

The saved search `SentinelOne Devices Lookup - Cleanup` runs every hour 39 minutes after the hour to remove old/stale device data from the [Splunk KVstore](https://docs.splunk.com/Splexicon:Appkeyvaluestore). By default, it will remove any device that has not reported in longer than 2 days.

???+ note
    Even though a device may be removed, it will be re-added by the saved search `SentinelOne Devices Lookup - Gen` if it begins to send data again.

## Update Search Macro

To change the retention period from the default 2 days, there is a search macro that will need to be updated.

1. Navigate to Settings > Advanced Search > Search Macros.
1. Set the "App" to `SA-SentinelOneDeviecs`.
1. Set the "Owner" to `Any`.
1. Click on `sa_sentinelone_retention` to modify the definition.
1. Set the definition to a valid [time modifier](https://docs.splunk.com/Documentation/Splunk/latest/SearchReference/SearchTimeModifiers#How_to_specify_relative_time_modifiers).

???+ important
    __Make sure to keep the quotes around the definition.__

    i.e.

    "-7d@d"

## Update Search Schedule

It may also be necessary to update how often the cleanup search runs (default: hourly).

To update the default schedule perform the following steps:

1. Navigate to Settings > Searches, reports, and alerts.
1. Set the "App" dropdown to `SA-SentinelOneDevices`.
1. Set the "Owner" dropdown to `All`.
1. Click "Edit" under actions for the search `SentinelOne Devices Lookup - Cleanup`
1. Click "Edit Schedule" and update the schedule and necessary.
