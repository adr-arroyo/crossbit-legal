---
permalink: /en/privacy.html
---

# CrossBit Privacy Policy

**Last updated:** 2 September 2026

This Privacy Policy explains how CrossBit ("the app", "we", "us") processes personal
data when you use the CrossBit mobile application on Android or iOS.

## 1. Controller

- **Controller:** Adrián Arroyo Pérez (individual)
- **Address:** Condesa Mencia, 123, 5C, Burgos, 09006, Spain
- **Privacy contact:** crossbitapp@gmail.com

For questions about this policy or the processing of your data, contact us at
crossbitapp@gmail.com.

## 2. Core principle: health data stays on your device

CrossBit is designed with a local-first approach. Your workouts, meals, body metrics,
chat history, plans, shopping lists, personal records, templates, preferences and
settings are stored locally on the device, primarily in the app's `localStorage`. A
local automatic backup may also exist on native devices. We do not generally
synchronize this data with a server.

Data leaves your device only when:

1. you use the cloud coach or a cloud AI-analysis feature and send a message, the
   necessary context or an image to obtain a response;
2. you create an account or use CrossBit Pro, so that we can process the identity,
   account status, subscription and usage data needed to provide those features;
3. you voluntarily report an AI response, which includes the content you choose to
   report; or
4. a system, browser or advertising provider processes the technical data needed for
   speech recognition or advertising when you activate those features and the build
   includes them.

## 3. Data we process, purposes and legal bases

### 3.1. Data stored only on your device

| Category | Examples | Storage |
|---|---|---|
| Workouts | WODs, sets, weights, heart rate and personal records | `localStorage` |
| Nutrition | Meals, macros, goals, diet plan and shopping list | `localStorage` |
| Health metrics | Weight, sleep, steps, recovery and readiness | `localStorage` |
| Coach conversations | Chat history and briefing | `localStorage` |
| Planning | WOD templates and schedules, plans and preferences | `localStorage` |
| Settings | Goals, language, consents and local-model configuration | `localStorage` |

We do not receive this data merely because it remains on your device. You can export
or import it from *Settings → My data* in JSON format. Exported files and the local
automatic backup remain under your control; CrossBit does not upload them to our
servers.

### 3.2. Account and authentication data

You can use CrossBit locally without creating an account. The cloud coach and
subscription features require a **Firebase Authentication** account. The current
version supports email/password registration and sign-in only; the email must be
verified before using the cloud coach or managing a subscription.

| Data | Purpose | GDPR legal basis |
|---|---|---|
| Email address | Create, authenticate and recover your account | Performance of a contract (Article 6(1)(b)) |
| Unique user identifier (`uid`) | Link your session, subscription, reports and usage limits | Performance of a contract (Article 6(1)(b)) |
| Verification status and technical session data | Protect the account and control cloud access | Performance of a contract (Article 6(1)(b)) and legitimate interest (Article 6(1)(f)) |

Firebase Authentication manages passwords; CrossBit does not receive or store the
password in plain text. Firebase may retain authentication data and the technical
information needed to maintain the session under its own privacy policy.

### 3.3. Account, subscription and usage data in our cloud services

To provide the cloud coach, apply quotas and manage CrossBit Pro, we process only the
minimum information needed in Firestore:

| Data | Purpose | Technical retention |
|---|---|---|
| `uid`, tier (`free`/`pro`) and Pro expiry | Authentication, access and account status | Until account deletion is completed, subject to applicable obligations |
| Subscription reconciliation metadata (event type, identifier and timestamp) | Apply purchase, renewal, transfer, refund or expiration changes in order | Until account deletion is completed or the applicable technical expiry |
| Monthly AI-unit counters | Apply limits and prevent abuse | Up to 40 days |
| Opaque idempotency receipts | Prevent duplicate logical charges when a request is retried | Up to 40 days |
| Technical purchase-webhook receipts | Process a RevenueCat delivery once | Up to 90 days |
| Technical deletion checkpoint | Resume, retry and verify account deletion | Minimal workflow record; the current implementation has no specific automatic expiry; no health or chat content |

Chat request bodies and responses are not stored in Firestore.

### 3.4. Payments and subscriptions

CrossBit Pro purchases are made through Google Play or the App Store. **RevenueCat**
technically manages the customer and subscription status so the service can recognize
the Pro tier. We do not receive or store your card or payment-method details. RevenueCat,
Google Play and Apple may retain their own records under their policies and applicable
tax or accounting obligations.

See the privacy policies of [RevenueCat](https://www.revenuecat.com/privacy),
[Google Play](https://policies.google.com/privacy) and
[Apple](https://www.apple.com/legal/privacy/).

### 3.5. Data sent to the cloud AI coach

When you use the cloud coach, your message and the necessary context—for example,
recent workouts, meals or metrics relevant to your question—are sent to **Gemini 3.7
Flash through Vertex AI (Google Cloud)** to generate a response. Images and other
files are sent only when you activate the relevant feature.

- Before the first transmission, we request specific consent for cloud AI. Without a
  verified session or that consent, the request is not sent.
- This consent to send data to cloud AI is independent from microphone/camera
  permissions, Health Connect, Google UMP advertising consent and any general consent;
  accepting one does not authorize the others.
- Our cloud proxy forwards the request and response in memory. It does not store the
  request body or response; its logs contain only technical metadata such as method,
  route, status, duration and `uid` for security and diagnostics.
- Google Cloud processes the content under the applicable Vertex AI terms. The service
  configuration may involve limited retention for caching or abuse monitoring; see
  Google Cloud's terms for those processes. CrossBit does not use coach content to
  create an activity history or to train its own models.

The current version does not offer a way to enter a personal Gemini API key (BYOK).
The cloud coach uses CrossBit's authenticated proxy; the on-device coach uses a
downloaded local model.

### 3.6. Voluntary reports of AI-generated content

If you tap **Report** on a coach response, you voluntarily send the response text, the
reason you select, the message identifier and the date. The report is associated with
your `uid`, used for moderation and safety, and automatically deleted within a maximum
of **30 days**, or earlier if you delete your account.

### 3.7. Camera, photos, microphone and speech recognition

| Permission or feature | Purpose | Processing |
|---|---|---|
| Camera or photo library | Photograph or attach meals and WODs | The photo is processed for the requested analysis and the result is stored locally. If you use cloud analysis, the image is sent to Vertex AI; CrossBit does not store the photo on its servers. |
| Microphone and speech recognition | Create entries or dictate messages | The system, browser or device may perform transcription. CrossBit receives the resulting text; if you send it to the cloud coach, it is treated as cloud-message data. |

These permissions are requested only when you activate the relevant feature and can
be revoked in your operating-system settings.

### 3.8. Health Connect (Android)

On Android, you may connect CrossBit to **Health Connect** and authorize access to
steps, sleep sessions, heart rate, resting heart rate and hydration. CrossBit uses this
data to show activity, recovery and trend metrics in the app. It does not write data
back to Health Connect or share it with other developers. The data remains on your
device unless you activate a cloud-coach feature that needs that context; section 3.5
then applies.

### 3.9. On-device AI models

You may optionally download models to run AI **locally**. Downloads may come from
**Hugging Face** and may require an access token that you provide. The token and
inference remain on your device; Hugging Face may process your IP address and download
data under its own privacy policy.

### 3.10. Contextual advertising

When a native release build has the advertising integration enabled, CrossBit may show
a contextual Google Mobile Ads banner only to Free accounts in Home, Plan Calendar and
Progress. Pro accounts do not see banners. We do not use health, workout, nutrition,
readiness, email or Firebase `uid` data to target ads, and the app does not request
cross-app tracking or IDFA.

Google UMP requests or updates consent before ads are loaded and provides **Privacy
options** in Settings when required in the user's region. Ad requests are configured
as non-personalized; Google may process technical data needed to serve and measure ads
under its policy.

## 4. Special categories of data

Workout, nutrition and body-metric data may constitute health data, a special category
under Article 9 GDPR. It is processed outside the device only when you activate and
use a cloud feature that needs that context, with the explicit consent requested
before transmission. You can prevent new transmissions by not using the cloud coach
and using local mode.

## 5. Recipients and processors

We do not sell your data. We share it only when necessary to provide the requested
feature, with providers acting in their respective roles:

| Provider | Role | Policy |
|---|---|---|
| Google (Firebase Authentication, Firestore, Cloud Run, Vertex AI and, if enabled, Mobile Ads/UMP) | Account, cloud metadata, AI inference and contextual advertising | [Google Privacy Policy](https://policies.google.com/privacy) |
| RevenueCat | Technical subscription and entitlement management | [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy) |
| Google Play / Apple App Store | Distribution and payment processing | [Google](https://policies.google.com/privacy) / [Apple](https://www.apple.com/legal/privacy/) |
| Hugging Face | Optional download of local models | [Hugging Face Privacy](https://huggingface.co/privacy) |

The speech-recognition provider may vary depending on the operating system or browser
you use.

## 6. International transfers

Some providers may process data outside the European Economic Area, including in the
United States. Where applicable, transfers rely on safeguards provided by applicable
law, such as Standard Contractual Clauses or the EU–US Data Privacy Framework,
depending on the provider and service. Vertex AI inference may be configured in EU
regions.

## 7. Retention periods

| Data | Retention |
|---|---|
| Local workouts, meals, metrics, chat and planning | Until you delete them or uninstall the app; exported copies remain where you save them |
| Technical account profile | Until account deletion is completed, subject to applicable obligations |
| Usage counters and idempotency receipts | Up to 40 days, unless deleted earlier |
| Technical purchase-webhook receipts | Up to 90 days, unless deleted earlier |
| Voluntary AI-content reports | Up to 30 days, unless deleted earlier |
| Technical deletion checkpoint | While needed to complete, retry or verify the workflow; the current implementation has no specific automatic expiry |
| RevenueCat, Google Play and App Store records | Under those providers' policies and applicable tax or accounting obligations |
| AI-provider retention | Under the applicable Vertex AI terms and configuration |

## 8. Your rights and how to delete your data

Depending on the circumstances, you may exercise rights of access, rectification,
erasure, restriction, objection, data portability and withdrawal of consent.

- **Access and portability:** export your data from *Settings → My data → Export my
  data* in JSON format.
- **Local erasure:** use *Settings → My data → Delete local data*. This deletes the
  device records, settings and local automatic backup, but does not change your cloud
  account.
- **Cloud-account erasure:** use *Settings → Account → Delete cloud account*. The
  workflow requests reauthentication and confirmation and deletes the cloud data
  described in the [account-deletion policy](https://adr-arroyo.github.io/crossbit-legal/en/delete-account.html).
- **Request without the app:** use the [public deletion page](https://adr-arroyo.github.io/crossbit-legal/en/delete-account.html)
  or email crossbitapp@gmail.com from the address associated with the account.
- **Other rights or complaints:** contact crossbitapp@gmail.com.

You may also lodge a complaint with the competent supervisory authority. In Spain,
this is the [Spanish Data Protection Agency (AEPD)](https://www.aepd.es/).

## 9. Children

CrossBit is not directed at children under 18 and we do not knowingly collect data
from children. If you believe a child has provided us with data, contact us so that we
can delete it.

## 10. Security

We apply reasonable technical and organisational measures, including encryption in
transit (HTTPS/TLS), short-lived authentication tokens, Firestore access only through
the authorised proxy, diagnostics without sensitive content and no private API keys in
the cloud-mode build. No system is completely secure, but we work to protect your
data.

## 11. Changes to this policy

We may update this policy. We will publish the current version at
https://adr-arroyo.github.io/crossbit-legal/en/privacy.html with its update date and,
where changes are material, notify you in the app.

## 12. Contact

Adrián Arroyo Pérez — crossbitapp@gmail.com — Condesa Mencia, 123, 5C, Burgos, 09006,
Spain.
