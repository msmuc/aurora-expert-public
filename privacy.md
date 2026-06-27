---
layout: default
title: Aurora Expert — Privacy Policy
description: Privacy policy for the Aurora Expert iOS app.
---

# Aurora Expert — Privacy Policy

<p class="muted">Last updated: 27 June 2026</p>

Aurora Expert (“the app”) is a northern-lights forecasting app. We designed it to be
**privacy-preserving by default**: there are no accounts, no analytics, no advertising, and no
tracking. This policy explains what data the app uses and why.

## Summary

- **We do not collect personal information for our own use.** The app has no user accounts and no analytics SDK.
- **We do not track you** across apps or websites, and we do not sell or share data with data brokers.
- The only data leaving your device is (a) your location sent to **Apple WeatherKit** to fetch local cloud cover, (b) a **coarse region code** used to deliver optional aurora alerts, and (c) your device’s **push token** registered with Firebase Cloud Messaging.

## Information the app uses

### Location

- **On-device forecast.** Your precise location is used on your device to compute whether the aurora is visible where you are (sun/darkness, your geomagnetic latitude, light pollution).
- **Cloud forecast (Apple WeatherKit).** To show cloud cover, your location is sent to Apple’s WeatherKit service, governed by Apple’s privacy policy.
- **Optional aurora alerts.** If you enable alerts, your location is converted **on your device** into a coarse geographic region (roughly a 5°-latitude × 15°-longitude band), and only that region code is used to subscribe you to a notification topic. **Your precise coordinates are never uploaded to our servers.**
- Location access uses the “While Using the App” permission and can be revoked at any time in iOS Settings.

### Push notification token

- If you enable alerts, the app registers a **push token** with Firebase Cloud Messaging (a Google service) so your device can receive aurora notifications for your region’s topic. The token identifies the device, not you. We do not store it on our own servers or link it to your identity.

### Purchases

- Pro features are unlocked by a one-time in-app purchase, processed entirely by **Apple**. We never see or store your payment details; validation happens through Apple’s StoreKit.

### Data we do *not* collect

- No name, email, contacts, photos, or account.
- No advertising identifiers, no usage analytics, no crash analytics tied to you.

## Third-party data sources

Aurora Expert displays public space-weather and weather data from: **NOAA Space Weather Prediction
Center**, **NASA (CCMC/DONKI)**, the **GFZ Helmholtz Centre for Geosciences** (Hp30 index, CC BY 4.0),
and **Apple WeatherKit**. Fetching these feeds sends standard network requests (e.g. your IP address)
to those providers, governed by their respective policies.

## Data retention

We do not maintain a user database. Region notification subscriptions are anonymous topic
subscriptions and contain no personal data. Cached forecast data lives only on your device.

## Children

Aurora Expert is not directed at children and does not knowingly collect data from children under 13.

## Changes

We may update this policy; material changes will be reflected by the “Last updated” date above.

## Contact

Questions about this policy: [markey2000@googlemail.com](mailto:markey2000@googlemail.com)

---

<p class="muted">Need help using the app? See the <a href="./support.html">Support page</a>.<br>
Aurora Expert is an independent app and is not affiliated with NOAA, NASA, GFZ, or Apple.</p>
