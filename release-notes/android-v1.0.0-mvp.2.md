# Banger Booking Android MVP — Interface Refinement Build

Second standalone ARM64 Android test build, focused on making the MVP cleaner and usable on small phone screens.

## Interface refinements

- Correct Banger Booking logo on the launch screen
- Minimal Home screen with shorter, clearer copy
- Directory filters changed to State, City, and Genre dropdowns
- Searchable filter sheets with multi-select Genre support
- Responsive typography, cards, buttons, and long contact text
- Simplified Account, Map, venue detail, and Quick Pitch language
- Quick Pitch confirmation now makes clear that the user must review and send from their own email app

## Functionality retained

- Live Banger venue directory backed by the shared database
- Venue research pages and protected member-contact flow
- Email magic-link authentication and reusable Pitch Profile
- Quick Pitch handoff to the user's installed email app
- Native Google Places details module behind an explicit click-to-load action

## Validation

- ESLint passed
- Strict TypeScript passed
- 15 automated tests passed
- Expo Doctor passed 21 of 21 checks
- Small-phone browser render checked at 360 x 640 with no horizontal overflow
- Android ARM64 release build and release lint passed
- Package, version, architecture, and APK Signature Scheme v2 verified
- Google Places key verified blank, so this build cannot make a billable Places request

## Known activation gates

- Native Map is disabled until a restricted Android Maps key is approved and supplied.
- Google Places makes no request in this build; provider activation remains pending explicit cost approval.
- New production accounts currently remain pending because free registration is disabled.
- The Supabase mobile callback still requires production allowlist confirmation.
- Physical-device font scaling and multiple email-client handoff still require testing.

## Artifact

- File: `banger-booking-v1.0.0-mvp.2-arm64.apk`
- Size: 46,360,513 bytes
- SHA-256: `AD1669F47EEE6DD2C792A1BCDD2C22B5785FCF1510152D13BA295DC45E0C499D`
- Signing: local Android debug certificate; test installation only
