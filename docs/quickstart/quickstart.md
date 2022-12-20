# Quick Start

This add-on has a saved search and Asset configuration input enabled by default.

## Overview

1. [Updated default macro](#update-default-macro).
1. [Force initial build](#force-initial-build).
1. [Enable asset correlation](#enable-asset-correlation).
1. [Update category multivalue limit](#update-category-multivalue-limit).
1. <small>(optional)</small> [Update default saved search schedule](#update-default-saved-search-schedule).
1. <small>(optional)</small> [Disable existing asset sources](#disable-existing-asset-sources).

## Update default macro

!!! danger "[Danger, Will Robinson](https://cultural-phenomenons.fandom.com/wiki/Danger,_Will_Robinson)"
    Failure to update the macro to the correct setting will cause no devices to be available in Splunk Enterprise Security.

Macro | Default | Description
----- | ------- | -----------
`sa_sentinelone_index` | index=sentinelone | Index definition for SentinelOne devices index.

### Update Macro Procedure

!!! note "Update the index definition to the correct index that contains the `sentinelone:channel:agents` sourcetype."

Perform **_one_** of the following:

1. <small>(recommended)</small> Update via Splunk ES [General Settings](#es-general-settings).
1. Update via [Macro Definition](#macro-definition).

#### ES General Settings

<small>option 1 (recommended option)</small>

1. <small>(In Splunk Enterprise Security)</small> Navigate to Configure > General > General Settings.
1. From the "App" dropdown select `SA-SentinelOneDevices`.
1. Update the SA-SentinelOneDevices Index definition and click "Save."

---

#### Macro Definition

<small>option 2</small>

1. Navigate to Settings > Advanced Search > Search Macros.
1. From the "App" dropdown choose `SA-SentinelOneDevices`.
1. Set the "Owner" dropdown to `any`.
1. Click the macro named `sa_sentinelone_index` to update the index definition.

---

## Force Initial Build

The initial build of the SentinelOne assets will not occur until the first scheduled runtime (see [Update default saved search schedule](#update-default-saved-search-schedule)). To force the initial build perform the following:

1. Navigate to Settings > Searches, reports, and alerts.
1. Set the "App" dropdown to `SA-SentinelOneDevices`.
1. Set the "Owner" dropdown to `All`.
1. Click "Run" under actions for the search `SentinelOne Devices Lookup - Gen`.

!!! note
    The search will run in a new tab over the default time period of 60 minutes. Expand the timeframe to a larger window if the number of hosts in the last 60 minutes does not seem accurate. The default search is configured to run hourly to continually append new devices reported from SentinelOne.

---

## Enable asset correlation

Confirm asset correlation has been setup in Enterprise Security.

1. Navigate to Enterprise Security > Configure > Data Enrichment > Asset and Identity Management.
1. Switch to the "Correlation Setup" tab.
1. Either enable for all sourcetypes <small>(Recommended)</small> or selectively by sourcetype.
    - If you choose to enable select sourcetypes, ensure the `stash` sourcetype is also selected so Notable events will be enriched with asset information.
1. Save.

---

## Update category multivalue limit

By default, Splunk Enterprise Security limits the values for the category field to 25. This add-on has around 30 values for the category field, which will shorten to 25 unless the default is updated.

To increase the default limit, perform the following:

1. From Enterprise Security, navigate to Configure > Data Enrichment > Asset and Identity Management.
1. On the middle navigation, select "Asset Fields."
1. Click the category field from the table and increase the "Multivalue Limit" to __40__.

---

## Disable existing asset sources

!!! info "optional"

It may be possible that you have existing Asset Lookups defined. If SentinelOne is widely deployed in your environment the existing lookups may no longer be needed.

---

## Update default saved search schedule

!!! info "optional"

The default saved search runs on the 29th minute of every hour to update and continually build the SentinelOne assets. To update the default schedule perform the following steps:

1. Navigate to Settings > Searches, reports, and alerts.
1. Set the "App" dropdown to `SA-SentinelOneDevices`.
1. Set the "Owner" dropdown to `All`.
1. Click "Edit" under actions for the search `SentinelOne Devices Lookup - Gen`.
1. Click "Edit Schedule" and update the schedule and necessary.
