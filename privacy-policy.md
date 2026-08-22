# Privacy Policy

**Effective date:** 21 August 2026

Percy ("the App", "we", "us") is a personal recipe manager and meal planner developed by Harry Frith, an individual developer based in Australia. This policy explains what data the App collects, why, and what rights you have over it.

If you have questions about this policy or your data, contact **hfrith9@gmail.com**.

## 1. Information we collect

| Data | Why we collect it | Where it's stored |
|---|---|---|
| Email address | Account creation and sign-in | Supabase Auth |
| Password (if you sign up with email) | Account sign-in (stored as a salted hash — we never see or store it in plain text) | Supabase Auth |
| Name and email, if you sign in with Apple or Google | Account creation and sign-in, in place of a password | Supabase Auth (Apple/Google only ever send us a one-time identity token — we don't receive your Apple or Google password) |
| Name and nationality (required at sign-up) | Personalising the app and correctly weighting seasonal meal suggestions for your hemisphere | Supabase database |
| Contact details (optional) | Reaching you if needed; not required to use the App | Supabase database |
| Recipes you create or import (name, ingredients, steps, tags, ratings, cook history) | Core app functionality | Supabase database |
| Recipe photos you upload | Core app functionality | Supabase Storage |
| Recipe import source (a URL or text you paste, or photos of a recipe you take) | To extract recipe details on your behalf | Sent to Anthropic (see §3); not stored by us beyond the resulting recipe |
| Meal-plan notes (free text) | To parse your preferences into meal-planning constraints | Sent to Anthropic (see §3); not stored beyond the resulting plan |
| Push notification token (if you enable notifications) | Delivering reminders and household alerts to your device | Supabase database; the token itself (not any recipe/account content) is also sent to Expo's push notification service to deliver the notification — see §3 |
| Subscription/purchase status (Premium users only) | Unlocking Premium features on your account | Supabase database, populated via RevenueCat — see §3 |

We do not collect location data or contacts. We do not use advertising or analytics SDKs. We do use a payments SDK (RevenueCat, for anyone who subscribes to Premium) and, for signed-in Apple/Google users, those providers' own sign-in SDKs — both described in §3.

## 2. How we use your information

We use your data solely to provide the App's functionality: authenticating you, storing and displaying your recipes and meal plans, generating shopping lists, and (where you use the import feature) extracting recipe details from a link, pasted text, or photo.

**We do not sell your personal data, and we will not in the future.**

We plan to add crash and error reporting (for example, via a service like Sentry) to help us detect and fix bugs. This collects technical diagnostic data — such as device model, OS version, and a stack trace at the moment of a crash — not your recipes, photos, or account details.

We may also introduce advertising in the future to support a free tier. Advertising is a bigger step than crash reporting: it would likely involve device identifiers used for ad tracking, Apple's App Tracking Transparency prompt on iOS, and a consent banner for EU users, plus new third-party ad partners disclosed in §3. We haven't committed to this, and if we do, we will update this policy in advance and request your consent where required by law.

## 3. Third parties who process your data

We use a small number of service providers ("subprocessors") to run the App. None of them may use your data for their own purposes beyond providing their service to us.

- **Supabase** (database, authentication, and file storage). Supabase hosts our backend infrastructure. See [Supabase's privacy policy](https://supabase.com/privacy).
- **Anthropic** (recipe import parsing and meal-plan note parsing). When you import a recipe or write plan notes, the relevant text or photo is sent to Anthropic's Claude API to extract structured data. This happens through our own server-side function — Anthropic does not receive your email, password, or any data beyond what's needed for that specific request. Per Anthropic's commercial API terms, this data is not used to train Anthropic's models. See [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy).
- **TikTok** (oEmbed, TikTok imports only). If you import a recipe from a TikTok link, we make an unauthenticated request to TikTok's public oEmbed endpoint to retrieve the video's caption. No account data is sent.
- **Apple** and **Google** (Sign in with Apple / Google Sign-In, if you choose to use them). If you sign in this way, Apple or Google authenticate you and send us a one-time identity token, plus your name and email the first time you authorize the App. See [Apple's privacy policy](https://www.apple.com/legal/privacy/) / [Google's privacy policy](https://policies.google.com/privacy).
- **Expo** (push notification delivery, if you enable notifications). Your device's push token — not your recipes, photos, or account details — is sent to Expo's push service so it can relay a notification to your device on our behalf. See [Expo's privacy policy](https://expo.dev/privacy).
- **RevenueCat** (subscription management, Premium users only). If you subscribe to Premium, RevenueCat manages the subscription and tells us (via a server-to-server webhook) your subscription status, so we know to unlock Premium features on your account. RevenueCat receives your purchase/transaction data and a Percy-generated app user ID — never your name, email, or recipe data. See [RevenueCat's privacy policy](https://www.revenuecat.com/privacy).
- **Apple App Store / Google Play** (payment processing, Premium users only). Your subscription payment itself — including any card or payment details — is handled entirely by Apple or Google; we and RevenueCat never see or store your payment details.

Your recipe data, photos, and plan data are otherwise stored only with Supabase and are not shared with any other party.

## 4. Photos you attach to a recipe — please note

This section is about the photo you attach to a saved recipe (e.g. a photo of the finished dish) — not photos you use to import a recipe (see §1 and §3, those are forwarded to our AI provider and not stored by us).

A recipe photo is stored in cloud storage at an address that is not published or listed anywhere, but **is not access-controlled** — anyone who obtains the exact photo address could view that image without signing in. Don't upload photos containing sensitive personal information (e.g. images that also capture faces, documents, or other identifying material in the background).

## 5. Household sharing

The App lets you form a household with other Percy users (e.g. family members you live with). If you join or create a household, your recipes, meal plan, and shopping list become visible to — and editable by — the other members of that household, and your display name is visible to them. This is the household feature working as intended, not a data leak. Your personal ratings of recipes, your account credentials, and your email are never shared with household members. Leaving a household stops this sharing going forward; content you already contributed to the household stays with the household rather than being deleted (see §7 for what account deletion does instead).

## 6. International data transfers

Our service providers (Supabase, Anthropic, Apple, Google, Expo, RevenueCat) may process and store data outside Australia, including in the United States. By using the App, you consent to this transfer. We rely on our providers' own safeguards (standard contractual clauses and equivalent mechanisms) for cross-border transfers.

## 7. Data retention and deletion

We retain your account data for as long as your account is active. You can delete your account and all associated data (recipes, photos, plan history) at any time from **Settings → Account → Delete Account**, or by emailing us at hfrith9@gmail.com. Deletion is permanent and cannot be undone. If you have an active Premium subscription, deleting your account does not cancel it — cancel separately via your Apple/Google account subscription settings. We may retain minimal records where required by law (e.g. to comply with a legal obligation).

## 8. Your rights

Depending on where you live, you may have the right to: access the personal data we hold about you; correct inaccurate data; request deletion; request a copy of your data in a portable format; object to or restrict certain processing; and lodge a complaint with your local data protection authority. To exercise any of these rights, email hfrith9@gmail.com or use the in-app tools where available. This applies regardless of your location, including to users in the European Economic Area under the GDPR and users in Australia under the Privacy Act 1988.

## 9. Children's privacy

The App is not directed at children, and we do not knowingly collect personal data from anyone under 16. If you believe a child has provided us with personal data, contact us and we will delete it.

## 10. Security

We use industry-standard measures to protect your data, including encryption in transit (HTTPS/TLS) and database-level access rules that restrict each user's data to their own account. No system is perfectly secure, and we cannot guarantee absolute security.

## 11. Changes to this policy

We may update this policy from time to time. Material changes will be reflected by an updated effective date at the top of this page. Continued use of the App after a change constitutes acceptance of the revised policy.

## 12. Contact

Harry Frith
hfrith9@gmail.com
