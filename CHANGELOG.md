## Change Log

### v3.1.2 (Sep 29, 2022)
* Improved stability regarding server responses.

### v3.1.1 (Aug 3, 2022)
* Added Report feature.
  - Added `Report(SBDReportCategory report_category, std::wstring report_description, std::function<void(SBDError*)> completion_handler)` in SBDBaseChannel.
  - Added `ReportUser(SBDUser& offending_user, SBDReportCategory report_category, std::wstring report_description, std::function<void(SBDError*)> completion_handler)` in SBDBaseChannel.
  - Added `ReportMessage(SBDBaseMessage* message, SBDReportCategory report_category, std::wstring report_description, std::function<void(SBDError*)> completion_handler)` in SBDBaseChannel.
  - Added enum class `SBDReportCategory` with `Suspicious`, `Harassing`, `Spam`, `Inappropriate` in SBDTypes.h.

### v3.1.0 (Apr 19, 2022)
* First release.
