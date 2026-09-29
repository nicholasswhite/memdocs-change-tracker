---
title: "Review Client App Protection Logs"
description: This topic describes how to configure Intune app protection policy (APP) logs.
ms.date: "2025-10-23T00:00:00Z"
ms.topic: troubleshooting
ms.reviewer: demerson
---

# Review Client App Protection Logs

Learn about the settings you can review in the app protection logs. Access logs by enabling Intune Diagnostics on a mobile client.

The process to enable and collect logs varies by platform:

- **iOS/iPadOS devices** - Use Microsoft Edge for iOS/iPadOS to collect logs. For details, see [Use Microsoft Edge for iOS and Android to access managed app logs](../configuration/configure-edge-ios-android.md#use-microsoft-edge-for-ios-and-android-to-access-managed-app-logs).

## Log files

- **Windows devices** - Use *MDMDiag* and event logs. See, [Collect MDM logs](https://learn.microsoft.com/en-us/windows/client-management/mdm-collect-logs) in the Windows client management content, and the blog [Troubleshooting Windows Intune Policy Failures](https://learn.microsoft.com/en-us/archive/blogs/configmgrdogs/troubleshooting-windows-10-intune-policy-failures).
- **Android devices** - Use Microsoft Edge for Android to collect logs. For details, see [Use Microsoft Edge for iOS and Android to access managed app logs](../configuration/configure-edge-ios-android.md#use-microsoft-edge-for-ios-and-android-to-access-managed-app-logs).

  > [!NOTE]
  >
  > On Android Fully Managed devices, in certain instances the Intune Company Portal app may be visible under all apps. This may happen when an app associated with an app protection policy is either not installed or not launched.

The following tables list the App protection policy setting name and supported values that are recorded in the log. In addition, each setting identifies the policy setting found within Microsoft Intune admin center. For detailed information on each setting, see [iOS/iPadOS app protection policy settings](ref-settings-ios.md) and [Android app protection policy settings in Microsoft Intune](ref-settings-android.md).

## iOS/iPadOS App protection policy settings

| Name | Value details | Setting in Microsoft Intune App Protection Policy |
| --- | --- | --- |
| AccessRecheckOfflineTimeout | x minutes | **Section**: Conditional launch **Setting**: Offline grace period with action Block access (minutes) |
| AccessRecheckOnlineTimeout | *x* minutes | **Section**: Access requirements **Setting**: Recheck the Access requirements after (minutes of inactivity) |
| AllowedIOSModelsElseBlock | x characters | **Section**: Conditional launch **Setting**: Device model(s) with action Allow specified (Block non-specific) |
| AllowedIOSModelsElseWipe | x characters | **Section**: Conditional launch **Setting**: Device model(s) with action Allow specified (Wipe non-specific) |
| AppActionIfUnableToAuthenticateUser | 0 = Block access 1 = Wipe data required | **Section**: Conditional launch **Setting**: Disabled account |
| AppPinDisabled | 0 = Require 1 = Not required | **Section**: Access requirements **Setting**: App PIN when device PIN is set |
| AppSharingFromLevel | 0 = None 1 = Policy Managed apps 2 = All apps | **Section**: Data protection **Setting**: Receive data from other apps |
| AppSharingToLevel | 0 = None 1 = Policy managed apps 2 = All app | **Section**: Data protection **Setting**: Send org data to other apps |
| AuthenticationEnabled | 0 = Not required 1 = Require | **Section**: Access requirements **Setting**: Work or school account credentials for access |
| ClipboardCharacterLengthException | x characters | **Section**: Data protection **Setting**: Cut and copy character limit for any app |
| ClipboardEncryptionEnabled | 0 = Disabled 1 = Enabled | No administrative control for this setting. |
| ClipboardSharingLevel | 0 = Blocked 1 = Policy managed apps 2 = Policy managed apps with paste in 3 = Any app | **Section**: Data protection **Setting**: Restrict cut, copy, and paste between other apps |
| ContactSyncDisabled | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Sync app with native contacts app |
| DataBackupDisabled | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Prevent backups |
| DeviceComplianceEnabled | 0 = False 1 = True | **Section**: Conditional launch **Setting**: Jailbroken/rooted devices |
| DeviceComplianceFailureAction | 0 = Block access 1 = Wipe data | **Section**: Conditional launch **Setting**: Jailbroken/rooted devices |
| DialerRestrictionLevel | 0 = None, do not transfer this data between apps 1 = A specific dialer app 3 = Any dialer app | **Section**: Data protection **Setting**: Transfer telecommunication data to |
| DictationBlocked | 0 = Allow 1 = Block | No administrative control for this setting. |
| DisableShareSense | N/A | N/A: Not actively used by the Intune service. |
| EnableOpenInFilter | 0 = Disabled 1 = Enabled | **Section**: Data protection **Setting**: Send Org data to other apps &gt; Policy managed apps with Open-In/Share filtering |
| FaceIDEnabled | 0 = Block 1 = Allow | **Section**: Access requirements **Setting**: Face ID instead of PIN for access (iOS 11+/iPadOS) |
| FileEncryptionLevel | 0 = When device is locked 1 = When device is locked and there are open files 2 = After device restart 3 = Use device settings | **Section**: Data protection **Setting**: Encrypt org data |
| FileSharingSaveAsDisabled | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Save copies of org data |
| GenmojiConfigurationState | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Genmoji |
| IntuneIdentityUPN | UPN of the Intune MAM user | N/A |
| ManagedBrowserRequired | 0 = False 1 = True | **Section**: Data protection **Setting**: Restrict web content transfer with other apps |
| ManagedLocations | A value that represents the number of managed storage locations to which the app can save data.  1 = OneDrive 2 = SharePoint 3 = OneDrive &amp; SharePoint 4 = Box 5 = OneDrive &amp; Box 6 = SharePoint &amp; Box 7 = OneDrive, SharePoint &amp; Box 32 = Local Storage 33 = Local Storage &amp; OneDrive 34 = Local Storage &amp; SharePoint 35 = Local Storage, OneDrive &amp; SharePoint 36 = Local Storage &amp; Box 37 = Local Storage, OneDrive &amp; Box 38 = Local Storage, SharePoint &amp; Box 39 = Local Storage, OneDrive, SharePoint &amp; Box 128 = Photo Library 129 = Photo Library &amp; OneDrive 130 = Photo Library &amp; SharePoint 131 = Photo Library, OneDrive &amp; SharePoint 132 = Photo Library &amp; Box 133 = Photo Library, OneDrive &amp; Box 134 = Photo Library, SharePoint &amp; Box 135 = Photo Library, OneDrive, SharePoint &amp; Box 160 = Photo Library, Local Storage 161 = Photo Library, Local Storage &amp; OneDrive 162 = Photo Library, Local Storage &amp; SharePoint 163 = Photo Library, Local Storage, OneDrive &amp; SharePoint 164 = Photo Library, Local Storage &amp; Box 165 = Photo Library, Local Storage, OneDrive &amp; Box 166 = Photo Library, Local Storage, SharePoint &amp; Box 167 = Photo Library, Local Storage, OneDrive, SharePoint &amp; Box | **Section**: Data protection **Setting**: Allow user to save copies to selected services |
| ManagedUniversalLinks | A list of universal links that allow data to be open in the corresponding managed apps | **Section**: Data protection **Setting**: Select managed universal links |
| MaxPinRetryExceededAction | 0 = Reset PIN 1 = Wipe data | **Section**: Conditional launch **Setting**: Max PIN attempts |
| MaxOsVersion | maximum OS version | **Section**: Conditional launch **Setting**: Max OS version with action Block access |
| MaxOsVersionWarning | maximum OS version | **Section**: Conditional launch **Setting**: Max OS version with action Warn |
| MaxOsVersionWipe | maximum OS version | **Section**: Conditional launch **Setting**: Max OS version with action Wipe data |
| MinAppVersion | "0.0" = no minimum app version anything else = minimum app version | **Section**: Conditional launch **Setting**: Min app version with action Block access |
| MinAppVersionWarning | "0.0" = no minimum app version. anything else = minimum app version | **Section**: Conditional launch **Setting**: Min app version with action Warn |
| MinAppVersionWipe | "0.0" = no minimum OS version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min app version with action Wipe data |
| MinOsVersion | "0.0" = no minimum OS version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min OS version with action Block access |
| MinOsVersionWarning | "0.0" = no minimum OS version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min OS version with action Warn |
| MinOsVersionWipe | "0.0" = no minimum OS version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min OS version with action Wipe data |
| MinSDKVersion | "0.0" = no minimum SDK version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min SDK version with action Block access |
| MinSDKVersionWipe | "0.0" = no minimum SDK version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min SDK version with action Block access |
| MinimumRequiredDeviceThreatProtectionLevel | 0 = Not configured 1 = Secured 2 = Low 3 = Medium 4 = High | **Section**: Conditional launch **Setting**: Max allowed device threat level |
| MobileThreatDefenseRemediationAction | 0 = Block access 1 = Wipe data | **Section**: Access requirements **Setting**: Max allowed device threat level action) |
| NonBioPassTimeOutRequired | 0 = Not required 1 = Require | **Section**: Access requirements **Setting**: Override Touch ID with PIN after timeout |
| NonBioPassTimeOut | x minutes | **Section**: Access requirements **Setting**: Override Touch ID with PIN after timeout &gt; Timeout (minutes of inactivity) |
| NotificationRestriction | 0 = Allow 1 = Block Org Data 2 = Block | **Section**: Data protection **Setting**: Org data notifications |
| OpenDataFromManagedLocations | A value that represents the number of managed storage locations to which the app can save data.  1 = OneDrive 2 = SharePoint 3 = OneDrive &amp; SharePoint 4 = Camera 5 = OneDrive &amp; Camera 6 = SharePoint &amp; Camera 7 = OneDrive, SharePoint &amp; Camera 8 = Local Storage 9 = Local Storage &amp; OneDrive 10 = Local Storage &amp; SharePoint 11 = Local Storage, OneDrive &amp; SharePoint 12 = Local Storage &amp; Camera 13 = Local Storage, OneDrive &amp; Camera 14 = Local Storage, SharePoint &amp; Camera 15 = Local Storage, OneDrive, SharePoint &amp; Camera 16 = Photo Library 17 = Photo Library &amp; OneDrive 18 = Photo Library &amp; SharePoint 19 = Photo Library, OneDrive &amp; SharePoint 20 = Photo Library &amp; Camera 21 = Photo Library, OneDrive &amp; Camera 22 = Photo Library, SharePoint &amp; Camera 23 = Photo Library, OneDrive, SharePoint &amp; Camera 24 = Photo Library &amp; Local Storage 25 = Photo Library, Local Storage &amp; OneDrive 26 = Photo Library, Local Storage &amp; SharePoint 27 = Photo Library, Local Storage, OneDrive &amp; SharePoint 28 = Photo Library, Local Storage &amp; Camera 29 = Photo Library, Local Storage, OneDrive &amp; Camera 30 = Photo Library, Local Storage, SharePoint &amp; Camera 31 = Photo Library, Local Storage, OneDrive, SharePoint &amp; Camera | **Section**: Data protection **Setting**: Allow users to open data from selected services |
| OpenDataIntoOrgDocumentsBlocked | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Open data into Org documents |
| OfflineWipeInterval | x days | **Note**: No administrative control for this setting. |
| PINCharacterType | 0 = Passcode 1 = Numeric | **Section**: Access requirements **Setting**: Pin type |
| PINEnabled | 0 = Not required 1 = Require | **Section**: Access requirements **Setting**: PIN for access |
| PINExpiryDays | x characters | **Section**: Access requirements **Setting**: PIN reset after number of days &gt; Number of days |
| PINMinLength | x characters | **Section**: Access requirements **Setting**: Select minimum PIN length |
| PINNumRetry | x attempts | **Section**: Conditional launch **Setting**: Max PIN attempts |
| PrintingBlocked | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Printing org data |
| ProtectAllIncomingUnknownSourceData | N/A | **Note**: Not actively used by the Intune service. |
| ProtectManagedOpenInData | 0 = False 1 = True | **Section**: Data protection **Setting**: Send org data to other apps is set to Policy Managed apps with Open-In/Share filtering when true. Note that this can also be set to 1 when Policy Managed Apps with OS sharing is enabled. |
| ProtocolExclusions | A list of app URL protocol schemes that allow data to be open in the corresponding unmanaged apps data | **Section**: Data protection **Setting**: Select apps to exempt |
| RequireFileEncryption | N/A | **Note**: Not actively used by the Intune service. |
| ScreenCaptureConfigurationState | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Screen capture |
| SimplePINAllowed | 0 = Block 1 = Allow | **Section**: Access requirements **Setting**: Simple PIN |
| SpecificDialerProtocol | URL protocol scheme for the specific dialer that is used for phone calls from managed apps | **Section**: Data protection **Setting**: Dialer App URL Scheme |
| ThirdPartyKeyboardsBlocked | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Third party keyboards |
| TouchIDEnabled | 0 = Block 1 = Allow | **Section**: Access requirements **Setting**: Touch ID instead of PIN for access (iOS 8+/iPadOS) |
| UniversalLinkExclusions | A list of universal links that allow data to be open in the corresponding unmanaged apps | **Section**: Data protection **Setting**: Select universal links to exempt |
| UnmanagedBrowserProtocol | URL protocol scheme for the unmanaged browser that is used to view managed web links | **Section**: Data protection **Setting**: Restrict web content transfer with other apps |
| WritingToolsConfigurationState | 0 = Allow 1 = Block | **Section**: Data protection **Setting**: Writing tools |

## Android App protection policy settings

| Name | Value details | Setting in Microsoft Intune App Protection Policy |
| --- | --- | --- |
| AccessRecheckOfflineTimeout​ | x minutes | **Section**: Conditional launch **Setting**: Offline grace period with action Block access (minutes) |
| AccessRecheckOnlineTimeout​ | x minutes | **Section**: Access requirements **Setting**: Recheck the Access requirements after (minutes of inactivity) |
| AllowedAndroidManufacturersElseBlock | Empty if not set​, otherwise list of allowed manufacturers | **Section**: Conditional launch **Setting**: Device manufacturers with action Allow specified (Block non-specified) |
| AllowedAndroidManufacturersElseWipe | Empty if not set​, otherwise list of allowed manufacturers | **Section**: Conditional launch **Setting**: Device manufacturers with action Allow specified (Wipe non-specified) |
| AllowedAndroidModelsElseBlock | Empty if not set​, otherwise list of allowed models | No administrative control for this setting. |
| AllowedAndroidModelsElseWipe | Empty if not set​, otherwise list of allowed models | No administrative control for this setting. |
| AndroidSafetyNetDeviceAttestationEnforcement | NOT_REQUIRED = not set BASIC_INTEGRITY = Basic Integrity BASIC_INTEGRITY_AND_DEVICE_CERTIFICATION = Basic Integrity and certified devices | **Section**: Conditional launch **Setting**: Play integrity verdict |
| AndroidSafetyNetDeviceAttestationFailedAction | BLOCK = Block access WARN = Warn WIPE_DATA = Wipe Data | **Section**: Conditional launch **Setting**: Play integrity verdict |
| AndroidSafetyNetRequiredEvaluationType | NONE = not set HARDWARE_BACKED = Check strong integrity | **Section**: Conditional launch **Setting**: Play Integrity verdict evaluation type |
| AndroidSafetyNetVerifyAppsEnforcementType | NOT_REQUIRED = not set REQUIRE_ENABLED = configured | **Section**: Conditional launch **Setting**: Require threat scan on apps |
| AndroidSafetyNetVerifyAppsFailedAction | BLOCK = Block access WARN = Warn | **Section**: Conditional launch **Setting**: Require threat scan on apps |
| AppActionIfSamsungKnoxAttestationRequired | NONE = not set BLOCK = Block access WIPE = Wipe data WARN = Warn | **Section**: Conditional launch **Setting**: Samsung Knox device attestation |
| AppActionIfDevicePasscodeComplexityLessThanHigh | NONE = not set BLOCK = Block access WIPE = Wipe data WARN = Warn | **Section**: Access requirements **Setting**: Require device lock |
| AppActionIfDevicePasscodeComplexityLessThanLow | NONE = not set BLOCK = Block access WIPE = Wipe data WARN = Warn | **Section**: Access requirements **Setting**: Require device lock |
| AppActionIfDevicePasscodeComplexityLessThanMedium | NONE = not set BLOCK = Block access WIPE = Wipe data WARN = Warn | **Section**: Access requirements **Setting**: Require device lock |
| AppActionIfAccountIsClockedOut | NONE = not set WARN = Warn BLOCK = Block access | **Section**: Conditional launch **Setting**: Non-working time |
| AppActionIfUnableToAuthenticateUser | NONE = not set BLOCK = Block access WIPE_DATA = Wipe apps | **Section**: Conditional launch **Setting**: Disabled account |
| AppPinDisabled | true = Not required false = Require | **Section**: Access requirements **Setting**: App PIN when device PIN is set |
| ApprovedKeyboards | List of approved keyboard bundle IDs required | **Section**: Data protection **Setting**: Select keyboards to approve |
| AppSharingFromLevel | BLOCKED = None MANAGED = Policy Managed apps UNRESTRICTED = All apps | **Section**: Data protection **Setting**: Receive data from other apps |
| AppSharingToLevel | BLOCKED = None MANAGED = Policy Managed apps UNRESTRICTED = All app | **Section**: Data protection **Setting**: Send org data to other apps |
| AuthenticationEnabled | false = Not required true = Require | **Section**: Access requirements **Setting**: Work or school account credentials for access |
| BiometricIdEnabled | 0 = Block 1 = Allow | **Section**: Access requirements **Setting**: Biometrics instead of PIN for access |
| BlockAfterCompanyPortalUpdateDeferralInDays | x days | **Section**: Conditional launch **Setting**: Max Company Portal version age (days) |
| BlockClockSttausWithGracePeriod | N/A | **Note**: Not actively used by the Intune service. |
| BlockScreenCapture | false = Allow true = Block | **Section**: Data protection **Setting**: Screen capture and Google Assistant |
| ClipboardCharacterLengthException | x characters | **Section**: Data protection **Setting**: Cut and copy character limit for any app |
| ClipboardSharingLevel | BLOCKED = Blocked MANAGED = Policy managed apps MANAGED_PASTE_IN = Policy managed apps with paste in UNMANAGED = Any app | **Section**: Data protection **Setting**: Restrict cut, copy, and paste between other apps |
| ConditionalEncryptionEnabled | false = Require true = Not required | **Section**: Data protection **Setting**: Encrypt org data on enrolled devices |
| ConnectToVPNOnLaunch | false = Enable true = Disable | **Section**: Data protection **Setting**: Start Microsoft Tunnel connection on app-launch |
| ContactSyncDisabled | false = Allow true = Block | **Section**: Data protection **Setting**: Sync app with native contacts app |
| DataBackupDisabled | false = Allow true = Block | **Section**: Data protection **Setting**: Prevent backups |
| DeviceComplianceEnabled | false = False true = True | **Section**: Conditional launch **Setting**: Jailbroken/rooted devices |
| DeviceComplianceFailureAction | BLOCK = Block access WIPE_DATA = Wipe data | **Section**: Conditional launch **Setting**: Jailbroken/rooted devices |
| DialerRestrictionLevel | 0 = None, do not transfer this data between apps 1 = A specific dialer app 2 = Any policy-managed dialer app 3 = Any dialer app | **Section**: Data protection **Setting**: Transfer telecommunication data to |
| DictationBlocked | false = Allow true = Block | No administrative control for this setting. |
| FileEncryptionKeyLength | 128 256 | No administrative control for this setting. |
| FileSharingSaveAsDisabled | false = Allow true = Block | **Section**: Data protection **Setting**: Save copies of org data |
| IntuneMAMPolicyVersion | version number | N/A |
| isManaged | true false | N/A |
| KeyboardsRestricted | true = Required false = Not required | **Section**: Data protection **Setting**: Approved keyboards |
| ManagedBrowserRequired | true = Microsoft Edge or Unmanaged browser false = Any app | **Section**: Data protection **Setting**: Restrict web content transfer with other apps. |
| ManagedLocations | A value that represents the number of managed storage locations to which the app can save data, separated by a semi-colon. ONEDRIVE_FOR_BUSINESS SHAREPOINT LOCAL | **Section**: Data protection **Setting**: Allow user to save copies to selected services |
| MaxPinRetryExceededAction | RESET_PIN = Reset PIN WIPE_DATA = Wipe data | **Section**: Conditional launch **Setting**: Max PIN attempts |
| MaxOsVersion | "0.0" = no maximum OS version anything else = maximum OS version | **Section**: Conditional launch **Setting**: Max OS version with action Block access |
| MaxOsVersionWarning | "0.0" = no maximum OS version anything else = maximum OS version | **Section**: Conditional launch **Setting**: Max OS version with action Warn |
| MaxOsVersionWipe | "0.0" = no maximum OS version anything else = maximum OS version | **Section**: Conditional launch **Setting**: Max OS version with action Wipe data |
| MessagingRedirectAppDisplayName | Messaging app name | **Section**: Data protection **Setting**: Messaging App Name |
| MessagingRedirectAppPackageId | Messaging app package ID | **Section**: Data protection **Setting**: Messaging App Package ID |
| MinAppVersion | "0.0" = no minimum app version anything else = minimum app version | **Section**: Conditional launch **Setting**: Min app version with action Block access |
| MinAppVersionWarning | "0.0" = no minimum app version. anything else = minimum app version | **Section**: Conditional launch **Setting**: Min app version with action Warn |
| MinAppVersionWipe | "0.0" = no minimum OS version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min app version with action Wipe data |
| MinOsVersion | "0.0" = no minimum OS version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min OS version with action Block access |
| MinOsVersionWarning | "0.0" = no minimum OS version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min OS version with action Warn |
| MinOsVersionWipe | "0.0" = no minimum OS version anything else = minimum OS version | **Section**: Conditional launch **Setting**: Min OS version with action Wipe data |
| MinPatchVersion | "0000-00-00" = no minimum Patch version anything else = minimum Patch version | **Section**: Conditional launch **Setting**: Min Patch version with action Block access |
| MinPatchVersionWarning | "0000-00-00" = no minimum Patch version anything else = minimum Patch version | **Section**: Conditional launch **Setting**: Min Patch version with action Warn |
| MinPatchVersionWipe | "0000-00-00" = no minimum Patch version anything else = minimum Patch version | **Section**: Conditional launch **Setting**: Min Patch version with action Wipe data |
| MinimumRequiredCompanyPortalVersion | "0.0" = no minimum Company Portal version anything else = minimum Company Portal version | **Section**: Conditional launch **Setting**: Min Company Portal version with action Block access |
| MinimumRequiredDeviceThreatProtectionLevel | NOT_SET = not defined in the policy SECURED = Secured LOW = Low MEDIUM = Medium HIGH = High | **Section**: Conditional launch **Setting**: Max allowed device threat level |
| MinimumWarningCompanyPortalVersion | "0.0" = no minimum Company Portal version anything else = minimum Company Portal version | **Section**: Conditional launch **Setting**: Min Company Portal version with action Warn |
| MinimumWipeCompanyPortalVersion | "0.0" = no minimum Company Portal version anything else = minimum Company Portal version | **Section**: Conditional launch **Setting**: Min Company Portal version with action Wipe data |
| MobileThreatDefenseRemediationAction | BLOCK = Block Access WIPE_DATA = Wipe data | **Section**: Conditional launch **Setting**: Max allowed device threat level |
| NonBioPassRequiredOnLaunch | N/A | **Note**: Not actively used by the Intune service. |
| NonBioPassTimeOut | x minutes | **Section**: Access requirements **Setting**: Override fingerprint with PIN after timeout &gt; Timeout (minutes of inactivity) |
| NonBioPassTimeOutRequired | false = Not required true = Require | **Section**: Access requirements **Setting**: Override fingerprint with PIN after timeout |
| NotificationRestriction | UNRESTRICTED = Allow BLOCK_ORG_DATA = Block Org Data BLOCK = Block | **Section**: Data protection **Setting**: Org data notifications |
| OpenDataFromManagedLocations | A value that represents the number of managed storage locations to which the app can save data, separated by a semi-colon. ONEDRIVE_FOR_BUSINESS SHAREPOINT CAMERA | **Section**: Data protection **Setting**: Allow users to open data from selected services |
| OpenDataIntoOrgDocumentsBlocked | false = Allow true = Block | **Section**: Data protection **Setting**: Open data into Org documents |
| PINCharacterType | PASSCODE = Passcode NUMERIC = Numeric | **Section**: Access requirements **Setting**: Pin type |
| PINEnabled | false = Not required true = Require | **Section**: Access requirements **Setting**: PIN for access |
| PINExpiryDays | x characters | **Section**: Access requirements **Setting**: PIN reset after number of days &gt; Number of days |
| PINMinLength | x characters | **Section**: Access requirements **Setting**: Select minimum PIN length |
| PINNumRetry | x attempts | **Section**: Conditional launch **Setting**: Max PIN attempts |
| PackageExclusions | Empty if no bundle IDs are configured, otherwise bundle IDs separated by a semi-colon | **Section**: Data protection **Setting**: Select apps to exempt |
| PinHistoryLength | x PIN values to maintain | **Section**: Access requirements **Setting**: Select number of previous PIN values to maintain |
| PolicyCount | number | N/A |
| PrintingBlocked | false = Allow true = Block | **Section**: Data protection **Setting**: Printing org data |
| RequireClass3Biometrics | false = Not required true = Require | **Section**: Access requirements **Setting**: Class 3 Biometrics (Android 9.0+) |
| ProtectedMessagingRedirectAppType | 0 = Any messaging app 1 = Any policy-managed messaging app 2 = A specific messaging app 3 = None, do not transfer this data between apps | **Section**: Data protection **Setting**: Transfer messaging data to |
| RequireDeviceLock | true = Required false = Not required | **Section**: Conditional launch **Setting**: Require device lock |
| RequireDeviceLockEnforcementType | BLOCK = Block access WIPE_DATA = Wipe required | **Section**: Conditional launch **Setting**: Require device lock |
| RequireFileEncryption | false = Not required true = Require | **Section**: Data protection **Setting**: Encrypt org data |
| RequirePinAfterBiometricChange | false = Not required true = Require | **Section**: Access requirements **Setting**: Override Biometrics with PIN after biometric updates |
| SimplePINAllowed | false = Block true = Allow | **Section**: Access requirements **Setting**: Simple PIN |
| SpecificDialerDisplayName | Dialer app name | **Section**: Data protection **Setting**: Dialer app name |
| SpecificDialerPackageID | Dialer app bundle ID | **Section**: Data protection **Setting**: Dialer App Package ID |
| TouchIDEnabled | false = Block true = Allow | **Section**: Access requirements **Setting**: Fingerprint instead of PIN for access (Android 9.0+) |
| UnmanagedBrowserDisplayName | Unmanaged web browser display name | **Section**: Data protection **Setting**: Unmanaged Browser name |
| UnmanagedBrowserPackageID | Unmanaged web browser package ID | **Section**: Data protection **Setting**: Unmanaged Browser ID |
| UserStatusPollInterval | N/A | **Note**: Not actively used by the Intune service. |
| UserStatusTimeoutInSeconds | N/A | **Note**: Not actively used by the Intune service. |

## Next steps

- To learn more about app protection policies, see [What are app protection policies?](overview.md)
- Intune offers a number of tools to help you troubleshoot issues in your environment. For more information, see [Use the troubleshooting portal to help users](../../fundamentals/it-pro-support/help-desk-operators.md).
