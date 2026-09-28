# Banger Booking Android Builds

Public delivery repository for installable Banger Booking Android test builds.

This repository is deliberately separate from both the Banger website and the Android application source. APK binaries are attached to GitHub Releases instead of committed into Git history. Each release includes its build type, supported architecture, signing status, validation summary, and SHA-256 checksum.

## Current build

- Release: `android-v1.0.0-mvp.3`
- Package: `com.pixeldustinteractive.bangerbooking`
- Version: `1.0.0` (`versionCode` 1)
- Android: API 24 minimum; API 36 target
- Architecture: ARM64
- Signing: local Android debug certificate; test installation only
- SHA-256: `A60E957710CE736DB4FCC594A64B295E191DBF7A92DF4E5F054C141BD9EB2A92`

Do not submit these test APKs to Google Play. Store delivery requires Play release signing and an Android App Bundle.
