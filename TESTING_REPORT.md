# TubeVolt-Yt Downloader — release verification

**Verification date:** 22 November 2026  
**APK display name:** TubeVolt  
**Version:** 1.0.0 (version code 1)

## Build and tests

Gradle completed successfully for `testGithubDebugUnitTest` and `assembleGithubRelease`. The unit suite ran 5 tests with 0 failures, 0 errors, and 0 skipped tests. The signed release APK was produced; its package/version/launcher-label metadata and signing certificate were verified.

## Lint

Release Lint completed with **0 errors and 171 warnings**. These are non-blocking findings, but they remain outstanding and should be reviewed during future maintenance. The build also reports deprecated API/Gradle features; some bundled native libraries could not be stripped and were packaged as-is.

## Functional scope and limits

Source/build review confirmed removal of the download-start interstitial; an ad gate while metadata fetches and active download/processing work are present; foreground-service continuation when the app task is removed; sticky restart and persisted-task recovery; duplicate-worker protection; preservation of user-paused tasks; and normal rather than background worker priority.

No Android device or emulator was attached. App installation/update, Recents-swipe continuation, process-death recovery, runtime UI, live network downloads, MP3/MP4 processing, notifications, power-management behavior, and store compatibility were **not** tested on-device. The unit tests do not verify ad timing or the service lifecycle end-to-end.

Android force-stop / Active apps Stop cannot be overridden. Device-maker task killers, power loss, network loss, and storage errors can interrupt work; in some circumstances, reopening the app may be needed to resume. These checks are not a guarantee that every device or download will work without issues.
