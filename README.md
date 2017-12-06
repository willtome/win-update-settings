# Windows Update Settings Ansible Role
This role is intended to configure and control the registry keys for Windows automatic updates. See the table below for for the default settings. For more information, see <https://msdn.microsoft.com/en-us/library/dd939844(v=ws.10).aspx>

## Variables for Windows Update
These values are registry keys configured in HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\WindowsUpdate

| variable | Default | Options |
| ---------| :-------------: | ------- |
| win_update_AcceptTrustedPublisherCerts | 1 | 1 = Enabled <br> 0 = Disabled |
| win_update_DisableWindowsUpdateAccess  | 0 | 1 = Disables <br> 0 = Enables |
| win_update_ElevateNonAdmins | 0 | 1 = All members <br> 0 = Only Admins |
| win_update_TargetGroup | Ansible | Only used if target group enabled |
| win_update_TargetGroupEnabled | 0 | 1 = Use client-side targeting <br> 0 = Do not use client-side targeting |
| win_update_WUServer | http://10.0.0.11:80 | HTTP(S) URL of WSUS Server |


## Variables for Automatic Update
These values are registry keys configured in HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\WindowsUpdate\AU

| variable | Default | Options |
| ---------| :-------------: | ------- |
| win_update_AUOptions | 2 | 2 = Notify before download <br> 3 = Automatically download and notify of installation. <br> 4 = Automatically download and schedule installation <br> 5 = Automatic Updates is required and users can configure it |
| win_update_AutoInstallMinorUpdates | 0 | 0 = Treat minor updates like other updates <br> 1 = Silently install minor updates |
| win_update_DetectionFrequency | 22 | Time between detection cycles. Time in hours (1–22) |
| win_update_DetectionFrequencyEnabled | 1 | 1 = Enable detection frequency <br> 0 = Disable. Use default value of 22 hours |
| win_update_NoAutoRebootWithLoggedOnUsers | 1 | 1 = Logged-on user can decide <br> 0 = Notify user that the computer will restart |
| win_update_NoAutoUpdate | 1 | 0 = Enable Automatic Updates <br> 1 = Disable Automatic Updates |
| win_update_RebootRelaunchTimeout | 10 | Time between prompts for a scheduled restart |
| win_update_RebootRelaunchTimeoutEnabled | 1 | 1 = Enable RebootRelaunchTimeout <br> 0 = Disable custom RebootRelaunchTimeout |
| win_update_RebootWarningTimeout | 5 | Length of the restart warning countdown |
| win_update_RebootWarningTimeoutEnabled | 1 | 1 = Enable <br> 0 = Disable |
| win_update_RescheduleWaitTime | 30 | Time Automatic Updates waits at startup before it applies updates |
| win_update_RescheduleWaitTimeEnabled | 0 | 1 = Enable RescheduleWaitTime <br> 0 = Disable RescheduleWaitTime |
| win_update_ScheduledInstallDay | 0 | 0 = Every day <br> 1 through 7 = the days of the week |
| win_update_ScheduledInstallTime | 0 | The time of day in 24-hour format (0–23) |
| win_update_UseWUServer | 0 | 1 = The computer gets its updates from a WSUS server <br> 0 = The computer gets its updates from Microsoft Update |
