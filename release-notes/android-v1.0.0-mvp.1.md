# Banger Booking Android MVP — Test Build 1

First standalone ARM64 Android test build. The APK includes its JavaScript bundle and does not require a development server.

## Included

- Branded Home, Directory, Map, and Account navigation
- Live Banger venue directory with name, location, and genre filtering
- Incremental venue loading and shared Directory/Map filter state
- Venue research pages and protected member-contact flow
- Email magic-link authentication and reusable Pitch Profile
- Quick Pitch handoff to the user's installed email app
- Explicit click-to-load gate for Google Places

## Validation

- ESLint passed
- Strict TypeScript passed
- 15 automated tests passed
- Expo Doctor passed 21 of 21 checks
- Android release lint passed
- APK Signature Scheme v2 verified

## Known activation gates

- Native Map is disabled until a restricted Android Maps key is approved and supplied.
- Google Places makes no request in this build; native provider activation remains pending.
- New production accounts currently remain pending because free registration is disabled.
- The Supabase mobile callback still requires production allowlist confirmation.
- This build has not completed physical-device accessibility and email-client testing.

## Artifact

- File: `banger-booking-v1.0.0-mvp.1-arm64.apk`
- SHA-256: `3C7F5AB7F03D756F2381BFA42D96C9352DBB5AA1F144DB7D7C3F8747F840770E`
- Signing: local Android debug certificate; test installation only
