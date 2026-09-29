# Banger Booking Android MVP — Interface Refinement Build

Fourth standalone ARM64 Android test build, focused on a simpler, more elegant phone interface and reliable compact-screen behavior.

## Interface refinements

- Correct Banger Booking logo and branded launch screen retained
- Home reduced to one dominant venue-search action with a quieter map action
- Shorter, clearer wording across Home, Directory, Map, Account, Pitch Profile, Quick Pitch, and venue research
- State / Province, City, and Genre remain full-width dropdown filters
- Rounded, consistent fields, cards, dropdowns, buttons, and selected states
- Directory cards tightened for faster scanning with two-line review previews
- Venue research links now use compact secondary actions rather than a wall of primary buttons
- Repeated logos removed from utility screens so titles and tasks start higher on the phone
- Technical network failures replaced with plain-language recovery guidance
- Bottom navigation labels constrained for compact screens and large Android text settings
- Shared content shell adds safe shrinking, bounded width, and consistent gutters to prevent horizontal overflow

## Functionality retained

- Live Banger venue directory backed by the shared database
- Venue research pages and protected member-contact flow
- Email magic-link authentication and reusable Pitch Profile
- Quick Pitch handoff to the user's installed email app
- Native Google Places details behind an explicit click-to-load action

## Validation

- ESLint passed
- Strict TypeScript passed
- 36 automated tests passed
- Home, Directory, filter sheet, Map fallback, and Account rendered at 320 x 640
- Document width stayed within the 320-pixel viewport on every tested MVP tab
- Android ARM64 release build and release lint passed
- Package `com.pixeldustinteractive.bangerbooking`, version `1.0.0`, versionCode `2`, target API 36, and ARM64-only architecture verified from the APK
- APK Signature Scheme v2 and Android debug signer verified
- Final merged APK contains only Internet, vibration, network-state, Wi-Fi-state, and the app-scoped dynamic-receiver permission
- Google Maps and Places keys remain blank, so this build cannot make a billable Google request

## Known activation gates

- Native Map is disabled until a restricted Android Maps key is approved and supplied.
- Google Places makes no request in this build; provider activation remains pending explicit cost approval.
- New production accounts currently remain pending, and the protected-contact RPC and Pitch Profile policies require paid access. The approved sign-up-to-Quick-Pitch journey needs a server-side access decision before activation.
- The Supabase mobile callback still requires production allowlist confirmation.
- Physical-device font scaling, TalkBack, and multiple email-client handoff still require testing.
- Production Privacy, Terms, and Support destinations still need approved URLs.

## Artifact

- [Download the APK from this GitHub repository](https://github.com/pixeldust-interactive/banger-booking-android-builds/raw/refs/heads/main/artifacts/banger-booking-v1.0.0-mvp.4-arm64.apk)
- File: `banger-booking-v1.0.0-mvp.4-arm64.apk`
- Size: 46,366,029 bytes
- SHA-256: `BBD93B6900973E6B89B46C6DBA4CBC092B2327459446F2DB39EA8E522EEF2131`
- Signing: local Android debug certificate; test installation only
