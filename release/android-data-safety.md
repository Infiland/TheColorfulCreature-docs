# Android Data safety draft for The Colorful Creature 1.2.0

Play Console saved this questionnaire as a **draft** on 24 September 2026. It has not been sent for review or made public. The existing published answer that the app collects no data was flagged invalid. Recheck this draft against the final uploaded AAB, the live privacy policy, and Google's current SDK guidance before submission.

The draft answers **Yes** to collection or sharing and says data is encrypted in transit. It states that the game has no Infiland account-creation flow; optional Google Play Games sign-in uses an existing Google account. The following six types are selected. Each is marked **collected and shared**, **not processed ephemerally**, and **required** because the AdMob SDK can collect data without a universal in-game opt-out in every region.

| Data type | Collected and shared for |
| --- | --- |
| Approximate location | Analytics; advertising or marketing; fraud prevention, security, and compliance |
| User IDs | App functionality; analytics; advertising or marketing; fraud prevention, security, and compliance; account management |
| Diagnostics | Analytics; advertising or marketing; fraud prevention, security, and compliance |
| Other app performance data | Analytics; advertising or marketing; fraud prevention, security, and compliance |
| App interactions | App functionality; analytics; advertising or marketing; fraud prevention, security, and compliance |
| Device or other IDs | Analytics; advertising or marketing; fraud prevention, security, and compliance |

The sources are [Google's Mobile Ads SDK disclosure guide](https://developers.google.com/admob/android/privacy/play-data-disclosure) and [Play Games Services disclosure guide](https://developer.android.com/games/pgs/data-collection), plus this project's `Obj_AdMob`, `scr_ads`, and `scr_platform_services` code. The Ads guide documents SDK 25.5.0 while this build packages 25.4.0. The game submits Play Games achievements and scores and stores the player ID locally to keep pending progress with the right account. AdMob collects IP address, product interactions, diagnostic information, and device or account identifiers for advertising, analytics, and fraud prevention.

The questionnaire preview displays all six types under both “Data shared” and “Data collected,” plus “Data is encrypted in transit.” The current Play privacy-policy URL is a Google Doc. A cross-platform game-specific policy is drafted at `../infi.land/public/the-colorful-creature-privacy.html`; it is not deployed or set as the Play policy URL. The upload-key reset is still pending, and no 1.2.0 AAB has been uploaded to Play.
