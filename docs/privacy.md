---
title: Privacy Policy
---

# Privacy Policy

**Last updated:** 2026-04-29

This Privacy Policy describes how **MyOwnStream** (the "App", "we", "us") handles
information when you use the App. By using MyOwnStream, you agree to this policy.

MyOwnStream is a **client application** for free catalog, m3U and xtream servers.
The App does provide free catalog from archive.org, but do not provide, host, or distribute any commercial media content. You connect the
App to your own server using credentials you obtain from your own provider.

---

## 1. What we DO NOT collect

We want to be clear about what we do **not** do:

- **No personal account** is required to use the App. You do not register with us.
- **No analytics, no tracking, no advertising SDKs.** We do not use Google
  Analytics, Crashlytics, AdMob, Facebook SDK, or similar tools.
- **No collection of your IPTV credentials on our servers** during normal use.
  Your server URL, username, and password are stored locally on your device.
- **No collection of your viewing history, favorites, or profile data on our
  servers** during normal use. They are stored locally on your device.
- **No selling or sharing of personal data with third parties** for marketing.

---

## 2. Data stored locally on your device

The App stores the following information **only on your device**, in its local
database (Room) and preferences:

- Server connection details you enter (URL, username, password)
- Profiles you create within the App
- Favorites, watch history ("Continue Watching"), and similar in-app activity
- App preferences (theme, language, etc.)
- Cached metadata fetched from your IPTV server (channel lists, posters, EPG)

This data **never leaves your device** unless you explicitly use the
**Sharing feature** described in Section 3.

If you uninstall the App, this local data is removed by the operating system
along with the App.

---

## 3. The Sharing feature (Firebase)

MyOwnStream offers an optional **Sharing feature** that allows you to share your
server connection and/or favorites with another person (for example, another
device you own, or a family member).

When — and only when — you actively trigger a share:

- The shared payload (server credentials and/or favorites list) is
  **[TODO: confirm: encrypted with AES-256 / encoded with Base64 / other]**
  before being sent.
- The payload is uploaded to **Google Firebase (Cloud Firestore / Realtime
  Database)** and stored under a short-lived share code.
- The recipient can retrieve the payload using that code.
- The payload is **automatically deleted** after **[TODO: e.g. 24 hours]** or
  immediately after being claimed, whichever comes first.

**We do not retain the payload beyond this window.** We do not log, read, or
process the contents of shared payloads — they are
**[TODO: confirm wording — "end-to-end encrypted" only if true]** and pass
through Firebase as opaque data.

If you never use the Sharing feature, **nothing is ever sent to Firebase by you
beyond the anonymous authentication described in Section 4.**

---

## 4. Firebase Anonymous Authentication

The App uses **Firebase Anonymous Authentication** to identify share sessions.
This means:

- An **anonymous, randomly generated user ID** is created on your device the
  first time the Sharing feature is initialized.
- This ID is **not linked to your name, email, phone, or any personal
  identifier**. We never ask for these.
- Firebase processes a minimal set of technical metadata required for
  authentication (e.g. an authentication token). See Google's privacy practices
  below.

You can sign out and reset this anonymous ID at any time from
**[TODO: e.g. Settings → Sharing → Reset]**.

---

## 5. Connections to your IPTV server

When you use the App, it makes network requests directly to **the IPTV server
you configured**. Those requests include your credentials and information about
what you watch. **This communication is between your device and your IPTV
provider — it does not pass through our servers.**

You should review the privacy policy of your IPTV provider, as they may log this
activity. We have no control over and no responsibility for your provider's
practices.

---

## 6. Permissions

The App requests the following Android permissions:

- **Internet / Network state** — required to communicate with your IPTV server
  and (when sharing) with Firebase.
- **[TODO: list any other permissions actually requested by your manifest, e.g.
  Foreground service for playback, Wake lock, Post notifications, External
  storage if any.]**

The App does **not** request access to your contacts, location, microphone,
camera, SMS, or call logs.

---

## 7. Third-party services

We use the following third-party services:

| Service | Purpose | Provider | Privacy policy |
|---|---|---|---|
| Firebase Anonymous Auth | Identify share sessions | Google LLC | https://firebase.google.com/support/privacy |
| Firebase **[TODO: Firestore / Realtime DB / Storage — keep only what you use]** | Temporary storage of share payloads | Google LLC | https://firebase.google.com/support/privacy |

Firebase processing may involve transfer of technical data to Google data
centers, including in the United States. Google participates in the EU-U.S.
Data Privacy Framework.

We do **not** use any other third-party SDK that processes personal data.

---

## 8. International users

The App is available worldwide. If you are located in the European Economic
Area (EEA), the United Kingdom, Switzerland, California, or another jurisdiction
with data protection laws, the rights described in Section 9 apply to you.

Because we do not collect personal data on our own servers (see Sections 1–4),
most data protection requests can be fulfilled by you directly: uninstalling
the App removes locally stored data, and shared payloads expire automatically.

---

## 9. Your rights

Depending on your jurisdiction, you may have the right to:

- **Access** the personal data we hold about you
- **Correct** inaccurate data
- **Delete** your data ("right to erasure" / "right to be forgotten")
- **Object to** or **restrict** processing
- **Data portability**
- **Withdraw consent** at any time
- **Lodge a complaint** with your local data protection authority

In practice, since we do not maintain user accounts and do not store personal
data on our servers beyond the temporary share payloads in Section 3, exercising
these rights generally means:

- **To delete locally stored data:** uninstall the App, or use in-app reset
  options if available.
- **To delete an active share:** wait for automatic expiry, or
  **[TODO: describe how the user can revoke a share, if possible]**.
- **For any other request:** contact us at the address below.

We respond to verifiable requests within **30 days**.

---

## 10. Children's privacy

MyOwnStream is not directed to children under **13** (or the equivalent minimum
age in your jurisdiction, e.g. 16 in parts of the EU). We do not knowingly
collect personal data from children. If you believe a child has provided us
with information through the Sharing feature, contact us and we will delete it.

---

## 11. Security

We rely on:

- **Local OS protections** for data stored on your device (Android
  app-sandboxing, file-system permissions).
- **TLS (HTTPS)** for traffic to Firebase.
- **[TODO: describe encryption used for the Sharing payload — e.g. "AES-256-GCM
  with a key derived from the share code, never sent to our servers"]**.

No method of transmission or storage is 100% secure. You are responsible for
keeping your device secure and for handling your IPTV credentials carefully.

---

## 12. Changes to this Privacy Policy

We may update this Privacy Policy from time to time. The "Last updated" date at
the top reflects the latest revision. Material changes will be highlighted in
the App or on this page. Continued use of the App after a change means you
accept the revised policy.

---

## 13. Contact

For privacy questions or to exercise your rights:

**Email:** myownlife.apps@gmail.com

**Developer:** My Own Stream
