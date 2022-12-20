# Release notes

## [v1.0.1 <small>December 20, 2022</small>](https://github.com/ZachChristensen28/SA-SentinelOneDevices/releases/tag/v1.0.1)

### Compatibility

Product | Version
--------- | -------
Splunk platform versions | 9.x, 8.x
Splunk Enterprise Security version | [7.x, 6.x](https://splunkbase.splunk.com/app/263)
SentinelOne App For Splunk | [5.1.x](https://splunkbase.splunk.com/app/5433)

### What's Changed

- Added managed configurations for ES - [#5](https://github.com/ZachChristensen28/SA-SentinelOneDevices/issues/5)
- Added managed settings for ES

**Full Changelog**: [v1.0.0...v1.0.1](https://github.com/ZachChristensen28/SA-SentinelOneDevices/compare/v1.0.0...v1.0.1)

## Known issues

Issue | Description | Solution | GitHub issue reference
----- | ----------- | -------- | ----------------------
Lookup file error | You may see the error `status="Lookup file error, unknown path or update time" name=sa_aws_assets` | This error exists since the KVstore is being used opposed to a csv file and does not interfere with the functionality of lookup creation. | Issue [#4](https://github.com/ZachChristensen28/SA-SentinelOneDevices/issues/4)

Issues can be reported on the [SA-SentinelOneDevices's GitHub page](https://github.com/ZachChristensen28/SA-SentinelOneDevices/issues).
