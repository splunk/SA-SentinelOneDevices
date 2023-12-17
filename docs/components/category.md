# Category Field

## Default category field mapping

Mapped Field | SentinelOne App For Splunk Event Field | Example value
------------ | ----------------------- | -------------
s1_active_threats | `activeThreats` | 4
s1_agent_version | `agentVersion` | 22.1.2.217
s1_allow_remote_shell | `allowRemoteShell` | false
s1_apps_vuln_status | `appsVulnerabilityStatus` | up_to_date
s1_detect_state | `detectionState` | full_mode
s1_device_type | `machineType` | desktop
s1_encrypted_apps | `encryptedApplications` | true
s1_external_ip | `externalIp` | 0.0.0.0
s1_firewall_enabled | `firewallEnabled` | true
s1_is_active | `isActive` | true
s1_is_decom | `isDecommissioned` | false
s1_is_infected | `infected` | false
s1_is_pending_uninstall | `isPendingUninstall` | false
s1_is_uninstalled | `isUninstalled` | false
s1_is_updated | `isUpToDate` | true
s1_last_active | `lastActiveDate` | 09/29/22 06:37:37 mdt
s1_last_scan | `scanFinishedAt` | 07/06/22 09:45:16 mdt
s1_last_updated | `updatedAt` | 02/14/22 09:52:05 MST
s1_last_user | `lastLoggedInUserName` | admin
s1_location_enabled | `locationEnabled` | true
s1_location_type | `locationType` | fallback
s1_mitigate_mode | `mitigationMode` | protect
s1_mitigate_mode_suspicious | `mitigationModeSuspicious` | detect
s1_model_name | `modelName` | red hat
s1_operational_state | `operationalState` | db_corruption
s1_os_name | `osName` | windows 10 enterprise
s1_os_type | `osType` | windows
s1_ranger_status | `rangerStatus` | enabled
s1_ranger_version | `rangerVersion` | 21.11.0.75
s1_remote_profile_state | `remoteProfilingState` | disabled
s1_sys_name | `modelName` | kvm
s1_threat_reboot_required | `threatRebootRequired` | false
splunk_last_updated | `now()` | 09/29/22 18:55:51 mdt

### Full example of category value

```yaml
gen:sa-sentinelone
s1_active_threats: 4
s1_agent_version: 22.1.2.217
s1_allow_remote_shell: false
s1_apps_vuln_status: up_to_date
s1_detect_state: full_mode
s1_device_type: desktop
s1_encrypted_apps: false
s1_external_ip: 0.0.0.0
s1_firewall_enabled: false
s1_is_active: true
s1_is_decom: false
s1_is_infected: false
s1_is_pending_uninstall: false
s1_is_uninstalled: false
s1_is_updated: true
s1_last_active: 09/29/22 06:37:37 mdt
s1_last_scan: 07/06/22 09:45:16 mdt
s1_last_updated: 09/29/22 06:27:32 mdt
s1_last_user: admin
s1_location_enabled: true
s1_location_type: fallback
s1_mitigate_mode: protect
s1_mitigate_mode_suspicious: detect
s1_model_name: red hat
s1_operational_state: db_corruption
s1_os_name: windows 10 enterprise
s1_os_type: windows
s1_ranger_status: enabled
s1_ranger_version: 21.11.0.75
s1_reomte_profile_state: disabled
s1_sys_name: kvm
s1_threat_reboot_required: false
splunk_last_updated: 09/29/22 18:55:51 mdt
```