# TubeVolt-Yt Downloader — release verification

**Verification date:** 22 November 2026  
**APK display name:** TubeVolt  
**Version:** 1.0.0 (version code 1)

## Build, tests, and Lint

The GitHub-flavor release APK was rebuilt successfully. Its metadata, launcher label, and signing certificate were verified. The GitHub unit suite ran 7 tests with 0 failures, 0 errors, and 0 skipped tests. Release Lint completed with **0 errors and 171 warnings**; the warnings remain for future maintenance review.

## Reviewed behavior

Source/build review confirmed standard display names for near-standard video heights while retaining the original selected-height constraint. On Download, the task is persisted and the foreground service is started before the start-ad attempt. The ad is shown promptly only if it is already loaded; otherwise it is skipped without holding the task. The regular active-work ad gate, service recovery, duplicate-worker protection, user-paused state, and normal worker priority remain in place.

## Device-test limits

No Android device or emulator was attached. Installation/update, Recents-swipe continuation, process-death recovery, runtime UI, live network downloads, MP3/MP4 processing, ad timing, notifications, power-management behavior, and store compatibility were **not** tested on-device. The unit tests do not exercise the service lifecycle, Unity Ads callbacks, or real downloads end-to-end.

Android force-stop / Active apps Stop cannot be overridden. Device-maker task killers, power loss, network loss, and storage errors can interrupt work; in some cases, reopening the app may be required to resume. These checks do not guarantee that every download or device will work without issues.
