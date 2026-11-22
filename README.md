# TubeVolt-Yt Downloader

**GitHub project/release title:** TubeVolt-Yt Downloader  
**Android app display name:** TubeVolt  
**Release:** 1.0.0 (version code 1)

TubeVolt is an Android video and audio downloader for supported media, with MP4/MP3 format choices and background download management. This public repository contains the original TubeVolt release APK and supporting documentation only. **Application source code is not published here**, and the Appteka-only clone APK is not distributed through this GitHub repository.

## Download

Download the signed original APK from the [latest GitHub release](https://github.com/simplefysakib/TubeVolt-Yt-Downloader/releases/latest). Its launcher label is **TubeVolt** and the version is `1.0.0` / code `1`.

## Quality and download behavior

Quality names are normalized to familiar tiers when a source height is only slightly different (for example, 1070 pixels is displayed as 1080p); the selected format retains its actual source-height constraint. When the Download button is pressed, the task is saved and sent to the foreground download service before the start interstitial is attempted. An already-loaded ad can appear promptly while the download proceeds; if no ad is ready, the app does not wait for it and continues the download.

Android force-stop / Active apps Stop, manufacturer power management, power loss, network problems, and storage failures can still interrupt a download. Background completion is not guaranteed on every device. See [release notes](RELEASE_NOTES_v1.0.0.md) and the [testing report](TESTING_REPORT.md).

## Verification and responsible use

The GitHub flavor's 7 unit tests passed. Release Lint reported 0 errors and 171 warnings. No device or emulator was available for Recents-removal, process-death, live-download, media-conversion, or ad-timing tests.

Download media only when you own it or have permission or another valid legal basis. Do not use the app to bypass DRM, authentication, paywalls, or other access restrictions. TubeVolt is independent and is not affiliated with, endorsed by, or sponsored by YouTube, Google LLC, or other content platforms. The notices here are general information, not legal advice or a guarantee against legal claims. Review the [legal notices](LEGAL_NOTICES.md), [privacy notice draft](PRIVACY_POLICY_DRAFT.md), and [third-party notices](THIRD_PARTY_NOTICES.md).

This repository contains no application source code and provides no explicit software reuse license. Publishing the APK does not grant rights to third-party media or software.
