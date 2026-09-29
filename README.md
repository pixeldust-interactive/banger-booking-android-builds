# Banger Booking Android Builds

Public delivery repository for installable Banger Booking Android test builds.

This repository is deliberately separate from both the Banger website and the Android application source. APK binaries are attached to GitHub Releases instead of committed into Git history. Each release includes its build type, supported architecture, signing status, validation summary, and SHA-256 checksum.

## Current build

- Release: `android-v1.0.0-mvp.4`
- Package: `com.pixeldustinteractive.bangerbooking`
- Version: `1.0.0` (`versionCode` 2)
- Android: API 24 minimum; API 36 target
- Architecture: ARM64
- Signing: local Android debug certificate; test installation only
- SHA-256: `BBD93B6900973E6B89B46C6DBA4CBC092B2327459446F2DB39EA8E522EEF2131`

Do not submit these test APKs to Google Play. Store delivery requires Play release signing and an Android App Bundle.
