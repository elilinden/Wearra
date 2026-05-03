# Privacy Policy

*Wearra · Effective April 20, 2026*

This Privacy Policy explains what information Wearra collects when you use the app, why we collect it, and the choices you have. We try to say this in plain English — if anything is unclear, email us at [batchcompressvideos@gmail.com](mailto:batchcompressvideos@gmail.com).

Wearra is operated by Eli Linden, a sole developer operating in the United States ("we," "us," or "Wearra").

## What we collect

### Information you give us directly

- **Account info.** When you sign in with Google, we receive your email address and display name. We assign you an internal user ID (a Firebase UID) that links your account to your data across the app's backend.
- **Photos you upload.** Wardrobe item photos, avatar photos, and garment photos you submit for virtual try-on rendering.
- **Wardrobe details.** Outfit notes, purchase prices, brand names, wear counts, tags, categories, and style preferences you enter.
- **Feedback.** Bad-render reports, attached photos, and any log bundles you choose to send through the in-app "Send to Developer" option.

### Device permissions we request

- **Camera.** To photograph clothing items and create your avatar.
- **Photo Library.** To import clothing photos and save try-on renders.
- **Location (while using the app).** For weather-appropriate outfit suggestions. We pass your latitude and longitude to Open-Meteo — no account identifier is sent.
- **Calendar (read-only).** To suggest outfits appropriate for your day's events. Calendar contents are read on-device; only the event titles for events you ask the assistant about are sent to Google's Gemini API for outfit suggestions. They are not stored on our servers.
- **Notifications.** For optional reminders and alerts (for example, when a render finishes).

You can revoke any of these at any time in iOS **Settings → Wearra**.

### Information collected automatically

- **Device information.** Device model, iOS version, app version, locale, and session length.
- **Crash reports.** Stack traces and non-fatal errors via Firebase Crashlytics.
- **Usage events.** Screen views and custom events (e.g., render start/finish, button taps) via Firebase Analytics.
- **Performance data.** Response times, render durations, and other performance metrics used to diagnose slowness and regressions.
- **Purchase history.** Records of your in-app subscription and top-up purchases, linked to your account, so we can unlock the features you paid for and reconcile credit balances. Apple handles the underlying payment data — we do not receive your credit card or Apple ID credentials.
- **Approximate location.** Country-level, derived from IP by Firebase Analytics. No precise GPS is sent with analytics events.
- **DeviceCheck token.** An opaque, per-device token provided by Apple's DeviceCheck. This is *not* your Apple ID, not the IDFA, and cannot be used to identify you across other apps. We use it only to store two bits of information per device to prevent abuse of our free-credits flow.

### Information stored only on your device

The following is stored locally on your iPhone using Apple's SwiftData framework and is not uploaded unless you explicitly use a feature that requires it:

- Your full wardrobe (photos, names, prices, brands, purchase dates, wear counts, tags, categories)
- Outfits and outfit history (compositions, hero images, notes)
- Packing trips
- Style preferences
- A cached snapshot of your profile (credit counts)

Uninstalling the app removes this data from your device.

### Information stored in our cloud (Google Firestore)

- `/users/{uid}` — email, display name, monthly render count, subscription snapshot
- `/users/{uid}/creditGrants/{id}` — credit history (amount, reason, source, timestamps)
- `/users/{uid}/badRenderReports/{id}` — photos, notes, item IDs, and the provider that produced the problematic render
- `/users/{uid}/logDumps/{id}` — optional log bundles you send via "Send to Developer"
- `/debug_logs/{id}` — render debug info (photos, provider, input params) generated when a try-on runs, so we can diagnose issues
- `/redeemCodes/{code}` — promo code state (we manage this; it isn't user-editable)

## How we use it

- **Virtual try-on rendering.** We send your avatar and garment photos to Google's Gemini and Vertex AI try-on models so they can generate the rendered image you requested.
- **AI chat and outfit suggestions.** Your prompts and the wardrobe context you share with the assistant are sent to Google Gemini 2.5 Flash.
- **Automatic item tagging.** When you add a clothing photo, it may be sent to Google Gemini for vision-based categorization (type, color, style).
- **Weather-aware suggestions.** Your coordinates are sent to Open-Meteo to fetch the local forecast.
- **Subscription management.** Apple handles billing; we receive subscription status through StoreKit so we can unlock Pro features.
- **Abuse prevention.** We use Apple's DeviceCheck to flag devices that have already claimed free starter credits, so the same iPhone cannot create unlimited free accounts.
- **Debugging and improvement.** Crash reports, usage analytics, and opt-in debug log uploads.
- **Support.** To respond when you email us.

We do not sell or share your personal information. We do not show ads. We do not use your photos to train AI models on our end, and Google receives photos only to return a render to you. Google's Gemini API terms (linked below) cover how that data is handled on their side.

## Third-party AI processing

Wearra uses Google's Gemini API to power its AI features. The following data is transmitted to Google for processing:

- Photos of you (avatar) and your clothing items, used for virtual try-on rendering and item tagging.
- Calendar event titles, used only when you request outfit suggestions for upcoming events.
- Approximate location and current weather conditions, used to suggest weather-appropriate outfits.

We do not transmit names, contacts, payment data, or other calendar metadata to Google. Per [Google's Gemini API terms of service](https://ai.google.dev/gemini-api/terms), data sent through the API is not used to train Google's AI models and is retained only for the time required to process the request and return a response.

Google's privacy practices are governed by their [privacy policy](https://policies.google.com/privacy). By using Wearra's AI features, you consent to your data being processed by Google under those terms in addition to ours.

## Third-party services

The following third parties receive data from Wearra in order for the app to function. Click a provider to open their privacy policy.

### Google

| Service | Purpose | Data shared |
|---|---|---|
| Firebase Authentication | Sign-in via Google OAuth | Email, display name |
| Firebase Firestore | User profile, credit records, reports, debug logs | Account data, uploaded photos, app events |
| Firebase Storage | Debug photo uploads when a render fails | Photos from the failed render |
| Firebase Remote Config | Feature flags and API keys delivered at runtime | App/device metadata only |
| Firebase Analytics | Usage events and device telemetry | Device model, iOS version, app version, locale, events, IP-derived country |
| Firebase Crashlytics | Crash and non-fatal error reporting | Stack traces, device state at crash |
| Google Cloud Functions | Server-side logic: `claimFreeCredits`, `redeemCode`, `submitBadRenderReport`, `alertWebhook` | Request payloads relevant to each function (e.g., DeviceCheck token, promo code, report content) |
| Google Gemini 2.5 Flash | Chat, outfit suggestions, and item categorization | Your prompts, wardrobe context, item photos for tagging, and — when you ask for event- or weather-aware suggestions — calendar event titles plus approximate location and weather |
| Google Gemini 2.5 Flash Image | Virtual try-on rendering | Avatar photo, garment photo(s) |
| Google Vertex AI (`virtual-try-on-001`) | Virtual try-on rendering | Avatar photo, garment photo(s) |

Google's privacy policy: [policies.google.com/privacy](https://policies.google.com/privacy). Firebase-specific details: [firebase.google.com/support/privacy](https://firebase.google.com/support/privacy).

### Apple

| Service | Purpose | Data shared |
|---|---|---|
| StoreKit 2 | Subscription and in-app purchase billing, refunds, receipts | Purchase receipts; Apple handles payment data |
| DeviceCheck | Abuse prevention (2 bits of state per physical device) | Opaque per-device token |
| Apple Push Notification service (APNs) | Delivery of push notifications | APNs device token |

Apple's privacy policy: [apple.com/legal/privacy](https://www.apple.com/legal/privacy/).

### Weather

| Provider | Purpose | Data shared | Policy |
|---|---|---|---|
| Open-Meteo | Local weather forecast for outfit suggestions | Latitude and longitude only — no identifier | [open-meteo.com/en/terms](https://open-meteo.com/en/terms) |

> **About retention on Google's side.** Once data reaches Google's Gemini API, retention and handling are governed by Google's terms (linked above). We do not separately control or store that data on Google's side.

## Your rights

### Everyone

- **Access:** request a copy of the data we hold about you.
- **Correction:** ask us to fix inaccurate data.
- **Deletion:** delete your account from within the app (**Settings → Danger Zone → Delete Account**), or email us and we'll do it for you. See "Account deletion and data retention" below for what happens next.

### California residents (CCPA / CPRA)

If you live in California, you have the right to:

- Know what personal information we collect, use, and disclose.
- Request deletion of your personal information.
- Correct inaccurate personal information.
- Opt out of the "sale" or "sharing" of your personal information. **We do not sell or share your personal information** as those terms are defined by the CCPA.
- Not be discriminated against for exercising these rights.

To exercise any of these rights, email [batchcompressvideos@gmail.com](mailto:batchcompressvideos@gmail.com). We verify requests using the email address associated with your account.

### EU / UK residents (GDPR / UK GDPR)

If you are in the European Economic Area, the United Kingdom, or Switzerland, you have the right to:

- Access your data and receive a copy in a portable format.
- Have your data corrected or erased.
- Restrict or object to processing.
- Withdraw consent at any time where processing is based on consent.
- Lodge a complaint with your local data protection authority.

Our legal bases for processing are: **contract** (to provide the try-on service you requested), **legitimate interest** (abuse prevention, debugging, improving the app), and **consent** (optional analytics and notifications where required). When your data is transferred outside the EEA/UK — for example, to our US-based backend or to Google's US-based Gemini API — we rely on standard contractual clauses or the provider's own transfer mechanisms.

## Data retention

- **Try-on photos.** Stored briefly during processing and removed from our Firebase Storage after the render completes or within 30 days, whichever is sooner. Retention on Google's side is governed by the Gemini API terms.
- **Account data.** Kept for as long as your account is active.
- **On-device data.** Your wardrobe, outfit history, and trip data stay on your iPhone and are removed when you uninstall the app.
- **Analytics and crash logs.** Retained according to Firebase's defaults (typically up to 14 months for analytics; shorter for crash logs).

### Account deletion and data retention

You may delete your account at any time from **Settings → Danger Zone → Delete Account**. When you do, your account enters a **30-day grace period**. During this period:

- You are signed out of the app on all devices.
- Your data is hidden from the app and inaccessible to you.
- We retain your data internally so we can respond to chargebacks, fraud claims, and support disputes.

After 30 days, all user-identifying data (profile, photos, outfits, credit history, reports) is permanently and irrevocably deleted. We retain a minimal audit record (email, deletion date) for up to 12 months for fraud prevention and regulatory compliance.

To cancel a scheduled deletion, email [batchcompressvideos@gmail.com](mailto:batchcompressvideos@gmail.com) within the 30-day window.

## Children's privacy

Wearra is not directed at children under 13, and we do not knowingly collect personal information from anyone under 13. If you believe a child under 13 has given us information, email [batchcompressvideos@gmail.com](mailto:batchcompressvideos@gmail.com) and we will delete it.

## Security

Data in transit is encrypted using TLS. Data at rest in Firebase is encrypted by Google. Access to our backend is restricted. No system is perfectly secure, but we take reasonable steps to protect your information.

## Changes to this policy

If we make material changes, we'll update the effective date at the top of this page and, for significant changes, show a notice inside the app the next time you open it. Continuing to use Wearra after the change means you accept the updated policy.

## Contact

Questions, requests, or concerns? Email [batchcompressvideos@gmail.com](mailto:batchcompressvideos@gmail.com). We respond within 3 business days.
