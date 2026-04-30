# AI-Outfits Support

We're a small, solo-developer operation. Here's how to get in touch and quick answers to common questions.

## Contact

- **Email:** [batchcompressvideos@gmail.com](mailto:batchcompressvideos@gmail.com)
- **Typical response time:** within 3 business days

When you email, it helps if you include: your account email, iPhone model + iOS version, what you were trying to do, and (if relevant) a screenshot.

## Frequently asked questions

### How do credits work?

Each virtual try-on render costs one credit.

- **Free tier:** 2 lifetime renders. They do not reset — once used, you'll need to subscribe to Pro or buy a top-up pack to keep rendering.
- **Pro subscription:** 30 renders per month. Renders reset at the start of each billing period.
- **5-render top-up pack:** a one-time $1.99 consumable available to Pro subscribers. Top-up credits stack on top of your monthly Pro allowance and never expire.

Your current credit balance is shown on the Home screen and in **Settings → Credits & Subscription**.

### What does the Pro subscription include?

Pro gives you 30 try-on renders per month, plus AI stylist chat and personalized outfit suggestions tied to your wardrobe. Pricing and renewal terms are always displayed before you confirm the purchase.

Pro is billed through your Apple ID as an auto-renewing monthly subscription, billed at $6.99/month, and renews until you cancel.

### I need more renders this month — can I buy extras?

Yes. You can buy a **5-render top-up pack** ($1.99) from the paywall. Top-up credits stack on top of your Pro allowance and never expire.

### How do I cancel my subscription?

Subscriptions are managed by Apple, not by us. To cancel:

1. Open the **Settings** app on your iPhone.
2. Tap your name at the top.
3. Tap **Subscriptions**.
4. Tap **AI-Outfits**.
5. Tap **Cancel Subscription**.

You'll keep Pro access until the end of the current billing period. You can also manage subscriptions at [apps.apple.com/account/subscriptions](https://apps.apple.com/account/subscriptions).

### How do I request a refund?

All charges are processed by Apple, so refunds come from Apple too. Request one at [reportaproblem.apple.com](https://reportaproblem.apple.com). If you think a charge is clearly wrong — for example, you were double-billed or the app failed to deliver what you paid for — email us and we'll help you with the request to Apple.

### A try-on render came out bad. What can I do?

AI-generated renders are not perfect. Unusual poses, busy backgrounds, tight crops, or uncommon garment types can trip up the model. A few things that help:

- Use a clear, front-facing avatar photo with good lighting.
- Use a garment photo on a plain background if possible.
- Try re-running the render — results vary each time.

If a render is badly broken, tap the **Report bad render** button on the result screen. Your report (the photos and your notes) helps us improve. For cases where a render clearly fails, email us and we'll credit you back.

### How do I delete my account and data?

Inside the app, go to **Settings → Danger Zone → Delete Account**. This starts a 30-day grace period:

- You're signed out on all devices.
- Your data is hidden from the app and inaccessible to you.
- We keep your data internally during that window to handle any chargebacks, fraud claims, or support disputes.

After 30 days, all user-identifying data (profile, photos, outfits, credit history, reports) is permanently deleted. We keep a minimal audit record (email + deletion date) for up to 12 months for fraud prevention and compliance.

If you change your mind during the 30-day window, email [batchcompressvideos@gmail.com](mailto:batchcompressvideos@gmail.com) and we'll cancel the deletion. If you can't access the in-app option at all, email us from the address linked to your account and we'll handle it manually.

Wardrobe items, outfits, and trip data stored locally on your iPhone are removed when you uninstall the app.

### Why didn't I get free credits on a new account?

We use an Apple technology called DeviceCheck to prevent the same iPhone from creating unlimited free accounts. It stores two bits of information on Apple's servers per device — it does not identify you and cannot be used to track you across other apps. It only tells us "this device has already claimed free starter credits."

If you believe this is a mistake (for example, you bought a used iPhone that had the app before), email us and we can look into it.

### What data does the app collect?

Short version: your email and display name (via Google Sign-In), photos you upload for try-on, the wardrobe items you enter, device/usage telemetry via Firebase Analytics, and crash logs via Firebase Crashlytics. Full details are in our [Privacy Policy](privacy.md).

### Where does my photo actually go when I render?

Your avatar and garment photo(s) are sent to Google's Gemini and Vertex AI try-on endpoints. Only the photos are sent — no email, display name, or account identifier is attached to the render call. Details are in our [Privacy Policy](privacy.md#third-party-services).

### Are my photos used to train AI models?

We don't train AI models on your photos. Your avatar and garment photos are sent to Google's Gemini API only to generate the render you requested. Per Google's Gemini API terms, data sent through the API is not used to train Google's models and is retained only for the time required to process the request — full details are in our [Privacy Policy](privacy.md#third-party-services).

### Why does the app want my calendar / location?

Both are optional. Calendar access is used to tailor outfit suggestions to your day; calendar contents are read on-device, and only the event titles for events you ask the assistant about are sent to Google's Gemini API for those suggestions. Location is used to fetch the weather forecast — your latitude and longitude are sent to Open-Meteo with no account identifier attached, and the resulting weather plus approximate location may be included in Gemini prompts when you ask for weather-aware suggestions.

You can revoke either permission at any time in iOS **Settings → AI-Outfits**.

### The app crashed / a feature isn't working.

First, make sure you're on the latest version from the App Store and your iPhone is running iOS 18 or later. If the issue persists, email us with your iPhone model, iOS version, and a description (screenshots help). Crash reports are automatically collected via Firebase Crashlytics.

### Is AI-Outfits available on Android or web?

Not right now. AI-Outfits is an iOS-only app for iPhone running iOS 18 or later.

### Is there a minimum age?

Yes — you must be at least 13 years old to use AI-Outfits.

## Legal

- [Privacy Policy](privacy.md)
- [Terms of Service](terms.md)
