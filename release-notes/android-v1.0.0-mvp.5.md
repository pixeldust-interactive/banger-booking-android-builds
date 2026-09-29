# Banger Booking Android MVP — Safe-Area Refinement Build

Fifth standalone ARM64 Android test build. This build preserves the simplified Banger interface from Build 4 and fixes content collisions with Android system bars during tab navigation and enlarged-text use.

## Interface refinement

- Uses the correct Banger Booking launch and Home branding
- Keeps State / Province, City, and Genre as full-width dropdown filters
- Applies explicit Android safe-area insets through the shared screen shell
- Prevents Home, Directory, Map, and Account headings from running beneath the status bar
- Keeps bottom content clear of the gesture/navigation area
- Retains compact cards, clear action hierarchy, plain-language errors, and the four-item MVP navigation

## Validation

- ESLint passed
- Strict TypeScript passed
- 37 automated tests passed
- Native x86_64 release APK built, installed, and launched on a 720 by 1280 small-phone Android emulator
- Home, Directory, Map, and Account visually passed at 200% Android font scaling
- Home passed again at normal font scaling after the fix
- Android logs contained no app crash or React Native JavaScript error during the tab checks
- ARM64 release build and release lint passed
- Package `com.pixeldustinteractive.bangerbooking`, version `1.0.0`, versionCode `3`, minimum API 24, and target API 36 verified from the APK
- APK Signature Scheme v2 and Android debug signer verified
- Google Maps and Places keys remain blank, so this build cannot make a billable Google request

## Known activation gates

- Native Map is disabled until a restricted Android Maps key, quota, and kill switch are approved.
- Google Places makes no request in this build; click-to-load remains implemented but inert without an approved key.
- New production accounts currently remain pending, and protected-contact and Pitch Profile policies require paid access. The sign-up-to-Quick-Pitch journey needs a server-side access decision before activation.
- The Supabase mobile callback still requires production allowlist confirmation.
- Physical-device, TalkBack, rotation, offline, lifecycle, and multiple email-client tests remain.
- Production Privacy, Terms, and Support destinations still need approved URLs.

## Artifact

- [Download the APK from this GitHub repository](https://github.com/pixeldust-interactive/banger-booking-android-builds/raw/refs/heads/main/artifacts/banger-booking-v1.0.0-mvp.5-arm64.apk)
- File: `banger-booking-v1.0.0-mvp.5-arm64.apk`
- Size: 46,366,145 bytes
- SHA-256: `3FA0D43C9CC96E78255F4897B8E2462BCF5B3CCB675965F5C5DE8B4B1FB8E13B`
- Signing: local Android debug certificate; test installation only
