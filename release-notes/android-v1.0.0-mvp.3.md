# Banger Booking Android MVP — Mobile Polish Build

Third standalone ARM64 Android test build, focused on removing narrow-screen defects and simplifying the core booking workflow.

## Interface refinements

- Correct Banger Booking logo retained on the launch screen
- State, City, and Genre remain simple, full-width dropdown filters
- Filter values can wrap instead of running off-screen at larger text sizes
- Bottom navigation grows with Android font scaling
- Venue cards and primary actions have clearer accessibility labels and disabled states
- Quick Pitch prevents duplicate email-app launches and keeps the draft available if handoff fails
- Pitch Profile now requires only artist name, a short introduction, and either a music or EPK link
- Optional genre and sign-off fields no longer block a pitch
- Obsolete filter-sheet code removed

## Functionality retained

- Live Banger venue directory backed by the shared database
- Venue research pages and protected member-contact flow
- Email magic-link authentication and reusable Pitch Profile
- Quick Pitch handoff to the user's installed email app
- Native Google Places details behind an explicit click-to-load action

## Validation

- ESLint passed
- Strict TypeScript passed
- 16 automated tests passed
- Expo Doctor passed 21 of 21 checks
- Home, Directory, Account, and filter-sheet renders checked at 360 x 640 and 320 x 640
- No horizontal overflow or viewport-crossing elements found at either tested width
- Android ARM64 release build and release lint passed
- Package, version, architecture, and APK Signature Scheme v2 verified
- Google Places key verified blank, so this build cannot make a billable Places request

## Known activation gates

- Native Map is disabled until a restricted Android Maps key is approved and supplied.
- Google Places makes no request in this build; provider activation remains pending explicit cost approval.
- New production accounts currently remain pending because free registration is disabled.
- The Supabase mobile callback still requires production allowlist confirmation.
- Physical-device font scaling and multiple email-client handoff still require testing.
- Production Privacy, Terms, and Support destinations still need approved URLs.

## Artifact

- File: `banger-booking-v1.0.0-mvp.3-arm64.apk`
- Size: 46,361,313 bytes
- SHA-256: `A60E957710CE736DB4FCC594A64B295E191DBF7A92DF4E5F054C141BD9EB2A92`
- Signing: local Android debug certificate; test installation only
