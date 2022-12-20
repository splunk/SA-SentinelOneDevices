# Release history

## [v1.0.0 <small>September 30, 2022</small>](https://github.com/ZachChristensen28/SA-SentinelOneDevices/releases/tag/v1.0.0)

### Compatibility

Product | Version
--------- | -------
Splunk platform versions | 9.x, 8.x
Splunk Enterprise Security version | [7.x, 6.x](https://splunkbase.splunk.com/app/263)
SentinelOne App For Splunk | [5.1.x](https://splunkbase.splunk.com/app/5433)

- Initial Creation

### Known issues

Issue | Description | Solution | GitHub issue reference
----- | ----------- | -------- | ----------------------
Lookup file error | You may see the error `status="Lookup file error, unknown path or update time" name=sa_aws_assets` | This error exists since the KVstore is being used opposed to a csv file and does not interfere with the functionality of lookup creation. | Issue [#4](https://github.com/ZachChristensen28/SA-SentinelOneDevices/issues/4)

Issues can be reported on the [SA-SentinelOneDevices's GitHub page](https://github.com/ZachChristensen28/SA-SentinelOneDevices/issues).
