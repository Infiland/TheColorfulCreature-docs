# The Colorful Creature iOS App Privacy inventory

This is a working disclosure inventory for the App Store Connect draft, not a published privacy label. The source is the signed iOS 1.2.0 (2) archive and current GameMaker code. Recheck it against the final production-ad build before publishing App Privacy.

On 23 September 2026, the eight categories below were saved in App Store Connect as a **draft**. The questionnaire's Publish action was not taken, and no policy URL was entered. The current draft marks Device ID as linked and used for tracking, matching the Google Mobile Ads manifest's potential tracking declaration. This makes the production ATT/ad configuration a release gate, not a completed implementation.

## Direct game behavior

| Data | Destination and purpose | Disclosure decision |
| --- | --- | --- |
| Campaign progress, settings, customization, queued scores and achievements | Local save files; continue play and retry eligible Game Center submissions | Local-only until a Game Center submission; local storage alone is not App Store “collection.” |
| Game Center player identifier | Received from Apple, stored in an account-specific local save filename; keeps pending submissions with the correct Game Center account | Assess the Game Center account ID and gameplay score/achievement data under Apple’s App Privacy definitions before finalizing. |
| Achievement and leaderboard records | Sent to Apple Game Center when signed in; shown there according to Game Center settings | App functionality; no Infiland game-account server. |
| `crash.txt` | Local file written on an exception | No automatic upload to Infiland. Support may receive it only if a player elects to send it. |
| Calendar time request | `timeapi.io` current-time endpoint | The service receives ordinary connection metadata such as IP. Check provider retention if classifying this as “collection.” |
| Optional news viewer | Steam news API and image hosts | Requests public content only; hosts receive connection metadata. Not an account or gameplay submission. |

## Bundled SDK manifests

The final archive contains the GameMaker app manifest, Google Mobile Ads SDK 12.0.0 manifest, and User Messaging Platform manifest. Google Mobile Ads declares Device ID, coarse location, advertising data, product interaction, performance data, crash data, and other diagnostic data. It marks Device ID as potentially used for tracking. UMP declares coarse location, performance data, and product interaction for app functionality. The app manifest declares file-timestamp access for save functionality, not collected data.

The shipped `Info.plist` has Google's **test** AdMob application ID and no `NSUserTrackingUsageDescription`; the code does not request App Tracking Transparency authorization. Therefore the final App Privacy questionnaire must not be completed by assuming that production personalized advertising and cross-app tracking are already correctly configured. Either ship a verified non-tracking ad setup or add a correctly timed ATT request and explain it consistently in the policy and App Privacy answers. Consent denial must continue to leave the game playable.

## Draft App Privacy categories to check in the UI

Based on the Google SDK manifests, expect **Identifiers / Device ID**, **Location / Coarse Location**, **Usage Data / Product Interaction and Advertising Data**, and **Diagnostics / Crash Data, Performance Data, Other Diagnostic Data**. Their collection purposes include third-party advertising, developer advertising, analytics, and UMP app functionality as indicated by the bundled manifests. Linked-to-user and tracking answers must be checked against actual production ad behavior, not copied blindly from the SDK's broad manifest. Review whether Game Center records add gameplay content and user ID categories under Apple's current questionnaire.

| Saved draft type | Purposes selected | Linked | Tracking |
| --- | --- | --- | --- |
| Coarse Location | Third-party advertising, developer advertising, analytics, app functionality | Yes | No |
| User ID | App functionality (Game Center account association) | Yes | No |
| Device ID | Third-party advertising, developer advertising, analytics | Yes | Yes |
| Product Interaction | Third-party advertising, developer advertising, analytics, app functionality | Yes | No |
| Advertising Data | Third-party advertising, developer advertising, analytics | Yes | No |
| Crash Data | Analytics | No | No |
| Performance Data | Third-party advertising, developer advertising, analytics, app functionality | No | No |
| Other Diagnostic Data | Third-party advertising, developer advertising, analytics | No | No |

Sources: `objects/Obj_AdMob/Create_0.gml`, `extensions/TCCPrivacy/iOSSource/TCCPrivacy.mm`, `scripts/scr_platform_services/scr_platform_services.gml`, `objects/o_getcalendartime/Create_0.gml`, `objects/o_newsviewer/Create_0.gml`, and the three `PrivacyInfo.xcprivacy` files in `~/Library/Caches/TCCPort/testflight/TCC-1.2.0-2-final.xcarchive/Products/Applications/The_Colorful_Creature.app/`.

The prepared game-specific policy is at `../infi.land/public/the-colorful-creature-privacy.html`. Its intended URL is `https://infi.land/the-colorful-creature-privacy.html` after deployment and live verification. Do not enter the URL in App Store Connect before it serves that file rather than the site's catch-all page.
