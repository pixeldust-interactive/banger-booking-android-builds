# Banger Booking Android MVP — Offline Recovery Build

Sixth standalone ARM64 Android test build. It retains the simplified Banger interface and safe-area corrections while replacing native connectivity exceptions with concise recovery guidance.

## Refinement

- Offline Directory failures now say: “We couldn’t load the directory. Check your connection and try again.”
- Raw Android errors such as `UnknownHostException` and hostname-resolution details are no longer shown to users.
- The existing **Try again** action restores live venue results after connectivity returns.
- The correct Banger Booking splash and Home branding, dropdown filters, compact visual hierarchy, and click-to-load Places gate remain intact.

## Validation

- ESLint passed
- Strict TypeScript passed
- 37 automated tests passed, including the exact Android `UnknownHostException` shape
- Expo Doctor passed all 21 checks
- Native x86_64 release build installed and ran on a 720 by 1280 small-phone Android emulator
- Airplane-mode Directory failure showed friendly copy and no raw exception
- Returning connectivity and pressing **Try again** removed the error and restored live venues
- Background/resume preserved the active Directory tab
- The portrait-only app safely ignored an OS rotation request and retained the active screen
- Android logs contained no app crash or React Native JavaScript error
- ARM64 release build and release lint passed
- Package `com.pixeldustinteractive.bangerbooking`, version `1.0.0`, versionCode `4`, minimum API 24, and target API 36 verified from the APK
- APK Signature Scheme v2 and Android debug signer verified
- Google Maps and Places keys remain blank, so this build cannot make a billable Google request

## Known activation gates

- Native Map is disabled until a restricted Android Maps key, quota, and kill switch are approved.
- Google Places makes no request in this build; click-to-load remains implemented but inert without an approved key.
- New production accounts currently remain pending, and protected-contact and Pitch Profile policies require paid access. The sign-up-to-Quick-Pitch journey needs a server-side access decision before activation.
- The Supabase mobile callback still requires production allowlist confirmation.
- Physical-device, TalkBack, and multiple email-client tests remain.
- Production Privacy, Terms, and Support destinations still need approved URLs.

## Artifact

- [Download the APK from this GitHub repository](https://github.com/pixeldust-interactive/banger-booking-android-builds/raw/refs/heads/main/artifacts/banger-booking-v1.0.0-mvp.6-arm64.apk)
- File: `banger-booking-v1.0.0-mvp.6-arm64.apk`
- Size: 46,366,501 bytes
- SHA-256: `149938564E0452B4D2FBD7F359320FC4877FE7DBA7641FAB0168A1643A7579F1`
- Signing: local Android debug certificate; test installation only
