---
layout: default
title: Aurora Expert — Privacy Policy
description: Privacy policy for the Aurora Expert iOS app.
lang: en
---

# Aurora Expert — Privacy Policy

<p class="muted"><a href="./privacy-de.html" hreflang="de">Deutsche Fassung</a></p>

<p class="muted">Last updated: 7 October 2026</p>

Aurora Expert ("the app") is a northern-lights forecasting app. We designed it to be **privacy-preserving by default**:
there are no accounts, no analytics, no advertising and no tracking. This policy explains what data the app uses, where
it goes and why.

## Controller

The developer of Aurora Expert.

Email: [markey2000@googlemail.com](mailto:markey2000@googlemail.com)

## Summary

- **We do not collect personal information for our own use.** The app has no user accounts and no analytics SDK. We
  (the developer) do not receive your location, your search terms or your purchases, and we do not record how you use
  the app. Apart from downloading two public data files we host on Google Firebase Storage (the global cloud layer and
  the alert status file – plain downloads that carry nothing about you beyond what every network request shows, such
  as your IP address), the only request that reaches our own server is a test alert you send yourself (see below).
- **We do not track you** across apps or websites, and we do not sell or share data with data brokers.
- Data leaves your device only to provide a feature you use:
  - **Apple WeatherKit** — coordinates, to fetch cloud cover;
  - **Apple Maps services (MapKit / Core Location)** — coordinates and search text, to find a place you type, to name
    places and look up their time zones, and to work out driving times;
  - **Google Firebase** — an installation identifier and a push token for notifications, the coarse region topics of
    your alert places, and, when you send a test alert, a random test topic with an App Check attestation;
  - **Apple** — purchases and the App Store rating dialog.

## Information the app uses

### Location
- **On-device forecast.** Your precise location is used on your device to compute whether the aurora is visible where
  you are (sun/darkness, your geomagnetic latitude, light pollution).
- **Cloud forecast (Apple WeatherKit).** To show cloud cover, the coordinates of your location — and of places you
  look at or save — are sent to Apple's WeatherKit service. The trip planner and "Tonight from here" also send the
  coordinates of a few candidate viewpoints around your accommodation or your current location (for "Tonight from
  here" at most eight per check, and only when you tap "Check"). Apple's handling of these requests is governed by
  Apple's privacy policy.
- **"Tonight from here".** If you have allowed location access, the app starts from a location fix of your device that
  is at most 30 minutes old; otherwise from your home place. This feature never asks for location access on its own.
- **Optional aurora alerts.** If you enable alerts, the location of your home place — and, with Aurora Pro, of each
  saved place that has alerts switched on — is converted **on your device** into a coarse geographic region (roughly a
  5°-latitude × 15°-longitude band). Only that region code, together with the alert threshold you chose, is used to
  subscribe to notification topics. **Your precise coordinates are never uploaded to our servers.**
- **Compass (field mode "I'm outside").** The compass heading and, with an existing location permission, coarse
  location fixes are used only on your device to point the arrow; they are not sent anywhere.
- Location access uses the "While Using the App" permission and can be revoked at any time in iOS Settings.

### Place search, place names, time zones and routes (Apple Maps services)
- **Place search.** When you search for a place — your home place, a saved place or the place you want to look at, and
  a base or accommodation in the trip setup — the text you type is sent to Apple's place search (`MKLocalSearch`, in
  the trip setup also `MKLocalSearchCompleter` for suggestions); the place you pick is resolved there too.
- **Names and time zones.** The app sends coordinates to Apple's reverse-geocoding service (Core Location / MapKit) to
  turn them into a place name and the place's time zone:
  - when you choose your current location as a place (your device's coordinates);
  - once after an update, for a place you chose in an earlier version that has no time zone stored yet;
  - for recommended destinations (trip planner, "Tonight from here") and, for "Tonight from here", for your device
    location when it is not one of your own places.
  Names of destinations are cached on your device, so the same point is not looked up again.
- **Driving times.** The trip planner and "Tonight from here" ask Apple's routing service (MapKit) for driving times
  between your base and candidate destinations.
- **"Start route"** opens Apple Maps with the destination you chose; from then on Apple Maps' own privacy policy
  applies.
- These requests go directly from your device to Apple. Apple's handling of them is governed by Apple's privacy
  policy. We receive none of it.

### Firebase and the push token
- When the app starts, it initialises Google Firebase (Cloud Messaging, App Check and Cloud Functions, no Analytics).
  Firebase creates an **installation identifier** for this copy of the app.
- Once you have allowed notifications — for aurora alerts or for trip reminders — the app registers with Apple's push
  service at every launch and passes the result to Firebase Cloud Messaging, which issues a **push token**. This can
  happen even if no alert is switched on.
- Aurora alerts are sent to topics. The app subscribes only the region topics described above (a coarse region and a
  threshold, never coordinates). The token identifies the app installation, not you. We do not store it on our own
  servers or link it to your identity.

### Test alert and Firebase App Check
- When you send a **test alert** from the Alerts tab, the app uses **Firebase App Check** (with Apple's App Attest or
  DeviceCheck) to prove to our server that the request comes from a genuine copy of the app. This happens only when you
  send a test alert, not at launch.
- The request goes to our server (a Firebase Cloud Function run by Google Cloud) and carries only the random,
  single-use test topic and the App Check token. Like any network request it shows your IP address to the server;
  Google Cloud's standard request logs for our project may record it. To prevent abuse, our server keeps a one-way hash
  of that random topic and the time of the request for about a day; this contains nothing that identifies you or your
  device.

### Notifications created on your device
- Trip departure reminders, their cancellation notices and the morning sighting question are **local notifications**
  scheduled by the app on your device. No server is involved.

### Journal photos, export and saving images
- **Adding photos** (Aurora Pro, "My nights"): you choose photos in the iOS photo picker. iOS hands the app only the
  photos you pick; the app gets no access to your photo library and asks for no permission for this.
- The app keeps **its own copy** of each picked photo in its storage on your device: a JPEG, at most 2048 pixels on the
  long side, **without location data (GPS)** and without the camera's capture metadata. The time the photo was taken
  is read once to match the photo to a night and stored with the journal entry. The original in your library stays
  as it is; deleting the copy in the app does not delete the original.
- The copies, like the rest of the journal, are part of your **device backup** (iCloud Backup or your computer) if you
  use one. The app itself never sends them anywhere; we (the developer) receive nothing.
- **Export** (CSV or JSON): only when you ask, the app writes your journal entries — without photos — to a file at a
  place you choose (for example the Files app). What happens to the file afterwards is up to you.
- **Sharing a card and "Save Image".** A card you share goes through the iOS share sheet to the app you choose. When
  you choose "Save Image", the app adds the card to your photo library; iOS asks once for permission to *add* photos
  (the app cannot read your library through it).

### Purchases
- Pro features ("Aurora Pro") are unlocked by a one-time in-app purchase, processed entirely by **Apple**. We never see
  or store your payment details. Purchase validation happens on your device through Apple's StoreKit.
- To show the "Founder" badge, the app reads the original purchase date of your Aurora Pro purchase **on your device**.
  It is not sent anywhere.
- Whether Aurora Pro is unlocked is also kept in the app's shared storage on your device, so the widgets can show Pro
  content.

### Rating request
- After you confirm a sighting in your journal, the app may ask iOS to show Apple's standard rating dialog. Whether it
  appears and what you enter there is handled by Apple.

### Data stored only on your device
Trip plans and their cached forecasts, place names, your sighting journal and the copies of its photos, the alerts
received on this device (the alert history), the last known forecast, settings,
counters (for example how many "Tonight from here" checks were made tonight), the state of a free storm-cockpit trial
and on-device performance reports (MetricKit) stay on your device. MetricKit reports appear only in the diagnostics
text you copy yourself; they are never uploaded.

### Data we do **not** collect
- No name, email, contacts or account. Photos you add to your journal stay in the app on your device (see "Journal
  photos" above); we never receive them.
- No advertising identifiers, no usage analytics, no crash analytics tied to you.

## Third-party data sources (informational)

Aurora Expert displays public space-weather and weather data from: **NOAA Space Weather Prediction Center**, **NASA
(CCMC/DONKI)**, the **GFZ Helmholtz Centre for Geosciences** (Hp30 index, CC BY 4.0), **Aurorasaurus** and **Apple
WeatherKit**. The global cloud layer and the alert status file are loaded from our **Google Firebase Storage** bucket.
Fetching these feeds sends standard network requests (for example your IP address) to those providers, governed by
their respective policies. Apart from the WeatherKit and Apple Maps requests described above, no location is attached
to these requests.

## Data retention

We do not maintain a user database. Region notification subscriptions are anonymous topic subscriptions and contain no
personal data. The test-alert hashes described above expire after about a day; Google Cloud's request logs for our
project are kept for Google Cloud's log retention period (by default 30 days). Cached forecast data and everything
listed under "Data stored only on your device" live only on your device and are removed when you delete the app.

## Your rights

Because we hold no personal data about you, there is usually nothing for us to access, correct or delete. You can
still contact us at the address above with any request under the GDPR (access, rectification, erasure, restriction,
objection, data portability), and you have the right to lodge a complaint with a data protection supervisory
authority. For data processed by Apple or Google, their respective privacy policies apply.

## Children

Aurora Expert is not directed at children and does not knowingly collect data from children under 13.

## Changes

We may update this policy; material changes will be reflected by the "Last updated" date above.

## Contact

Questions about this policy: [markey2000@googlemail.com](mailto:markey2000@googlemail.com)
