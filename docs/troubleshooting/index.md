# Troubleshooting

There can be many issues when setting up a new app/add-on in Splunk. Below highlights the most common issues with this Add-on. Don't see your issue? Submit a new issue on [GitHub](https://github.com/ZachChristensen28/SA-SentinelOneDevices/issues).

Issue | Description | Solution
----- | ----------- | --------
Multiple asset merge | It is possible that some of your devices share a common mac address or another key field which will cause merging by default. | If SentinelOne is your only asset source you can disable asset merge under global settings. See [Asset Merge Solution](./solution-guides/asset-merge) for more information.
Asset Database not populating with SentinelOne Data | The asset database may show no SentinelOne data if the initial search has not run to build the asset database or the default macro has not been updated. | Verify the default macro has the correct index definition (see [Update Default Macro](/quickstart/quickstart/#update-default-macro)). Also see [Force build](/quickstart/quickstart/#force-initial-build) to build the SentinelOne assets lookup before the first scheduled run.
Assets exceeding field limits | By default, Splunk Enterprise Security limits the values for the category field to 25. This add-on has around 30 values for the category field, which will shorten to 25 unless the default is updated. | [How to update multivalue field limit under the Quickstart guide](/quickstart/quickstart/#update-category-multivalue-limit)
