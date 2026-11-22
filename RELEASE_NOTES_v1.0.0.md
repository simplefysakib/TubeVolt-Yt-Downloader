# TubeVolt-Yt Downloader

**Android app display name:** TubeVolt  
**Version:** 1.0.0 (version code 1)

## Changes

- Removed the interstitial shown immediately after a download was queued.
- Suppressed interstitial display while metadata is being fetched or a download/processing task is active.
- Kept download execution in the foreground service when the app task is removed from Recents.
- Added sticky service restart handling and database-based recovery for queued, interrupted, and processing tasks; reopening the app also triggers recovery.
- Prevented duplicate worker dispatch for the same task and included processing tasks in duplicate-active checks.
- Raised service worker scheduling to normal Android priority rather than background priority.
- Corrected media-muxer sample-flag mapping and API-qualified navigation-bar theme attributes for Android compatibility.
- Preserved the requested version name `1.0.0`, version code `1`, app identity, and signing setup.

## Important limits

Android force-stop / Active apps Stop, manufacturer power-management policies, power loss, network failures, and storage errors can still interrupt downloads. Android does not allow an app to override force-stop or promise uninterrupted execution. The changes passed build and unit-test checks, but no connected device/emulator was available for install, Recents-swipe, process-kill, or live-download testing. Read `TESTING_REPORT.md` before relying on this build.
