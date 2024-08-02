## Change Log

### v3.1.10(Aug 2, 2024)
* Fixed crash issue during reconnect
* Fixed crash issue in `UpdateReadReceipt`

### v3.1.9(Jul 25, 2024)
* Removed duplicate definitions and unused declarations

### v3.1.8(Jul 17, 2024)
* Improved stability
* Updated Boost library

### v3.1.7(Jul 3, 2024)
* Fixed crash when parsing JSON

### v3.1.6(May 27, 2024)
* Added support for the Android x86_64 library

### v3.1.5(Apr 24, 2024)
* Added Ephemeral feature
  - Added `SetEphemeral(bool is_ephemeral)` in SBDGroupChannelParams
  - Added `SetEphemeral(bool is_ephemeral)` in SBDOpenChannelParams
* Improved stability

### v3.1.4(Apr 9, 2024)
* Added SendbirdChatPrivacyInfo.xcprivacy for Apple Privacy Manifest

### v3.1.3(Feb 23, 2024)
* Added support for Unreal 5.2

### v3.1.2 (Sep 29, 2022)
* Improved stability regarding server responses

### v3.1.1 (Aug 3, 2022)
* Added Report feature
  - Added `Report(SBDReportCategory report_category, std::wstring report_description, std::function<void(SBDError*)> completion_handler)` in SBDBaseChannel
  - Added `ReportUser(SBDUser& offending_user, SBDReportCategory report_category, std::wstring report_description, std::function<void(SBDError*)> completion_handler)` in SBDBaseChannel
  - Added `ReportMessage(SBDBaseMessage* message, SBDReportCategory report_category, std::wstring report_description, std::function<void(SBDError*)> completion_handler)` in SBDBaseChannel
  - Added enum class `SBDReportCategory` with `Suspicious`, `Harassing`, `Spam`, `Inappropriate` in SBDTypes.h

### v3.1.0 (Apr 19, 2022)
* First release
