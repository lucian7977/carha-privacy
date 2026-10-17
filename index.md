# CarHA — Privacy Policy

_Last updated: 17 October 2026_

CarHA is an Android app that controls your own smart-home devices from your
phone and from Android Auto. This policy describes exactly what the app does
with your data.

Contact: **apps.lucian7977@gmail.com**

## Short version

- There is **no CarHA account and no analytics or tracking server of ours**.
- Everything you configure is stored **locally on your device**.
- Every network request goes **directly to the services you configured**
  (your Home Assistant server, your MQTT broker, your eWeLink / Tuya / Shelly
  cloud accounts). Nothing is relayed through us.
- Location is used **only** for the geofence zones you create.

## What the app stores, and where

Everything lives in the app's private storage on your phone (Android
`SharedPreferences`). Nothing is uploaded anywhere by the app itself.

| Data | Why |
| --- | --- |
| Service credentials: Home Assistant URL and long-lived access token, MQTT host/port/username/password, eWeLink email/password, Tuya user code and tokens, Shelly authorization key and server URI | To call the services you added |
| Your tabs, button names, entity IDs, icons, colours and ordering | To build the dashboard the car shows |
| Geofence zones: name, latitude, longitude, radii, action and notification message | To register and trigger the zones |
| The "voice confirmation" preference | A local setting |

The app has no cloud sync and no user account. If you use "Export", the app
writes a JSON file containing all of the above — **including your credentials
and tokens** — to a location you pick with the system share/save dialog. That
file is only as private as the place you keep it.

## Permissions and what they are used for

**`INTERNET`, `ACCESS_NETWORK_STATE`**
Used to reach your Home Assistant instance, MQTT broker, and the eWeLink,
Tuya and Shelly endpoints. Requests go straight from your phone to those
servers. No proxy, no CarHA backend.

**`ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION`**
Used to (a) fill in the coordinates when you press "Use current location"
while creating a geofence zone, and (b) let Android fire the zone when you
cross its boundary. Location is read from the Google Play services fused
location provider and from the Android geofencing API. It is not sent
anywhere by CarHA itself.

**`ACCESS_BACKGROUND_LOCATION`**
Required so the zones keep working when the app is not on screen — which is
the normal case, because you want the gate to open while the phone is in your
pocket or the screen is off. Android's geofencing API delivers the
transition even when the app is backgrounded; without this permission zones
would only fire while the app is open. Adding a zone registers two system
geofences (an inner "action" radius and a larger outer "notification"
radius); turning the zone's switch off unregisters them.

**`FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_LOCATION`**
Android requires a short-lived foreground service so the process stays alive
for the few seconds between a geofence transition and the HTTP call the zone
fires. While it runs you will see the ongoing "Watching geofences"
notification.

**`POST_NOTIFICATIONS`**
Used for two things: the ongoing "Watching geofences" notification, and the
zone notification itself when you cross the outer radius (by default "You're
near <zone>. Activate: <action>?"). "Send test notification" in the app posts
one immediately. No notification content leaves the device.

## What we do **not** do

- No advertising SDK, no analytics SDK, no crash-reporting SDK.
- No account, no sign-up, no email address required.
- No selling or sharing of data with third parties.
- No access to your contacts, photos, microphone, camera or files beyond the
  backup file you choose to export.

## Third-party services you connect

CarHA is only a client. Once you add an account, the app sends requests to
that provider and the provider's own privacy policy applies:

- **Home Assistant** — your own server (or Nabu Casa cloud URL).
- **MQTT** — whichever broker host you typed in.
- **eWeLink / Sonoff** — eWeLink cloud API.
- **Tuya** — Tuya cloud API (EU / US / CN endpoint, as you choose).
- **Shelly** — your Shelly device or Shelly cloud server URI.

**Google Play services for location** is used through the Android geofencing
and fused-location APIs; the corresponding Google privacy policy applies to
those system services.

## Data retention and deletion

Nothing is kept on any server of ours, so there is nothing to expire. To
remove everything, delete the accounts/buttons in the app, use
"Delete application data" in Android settings, or uninstall the app. Any
exported backup file is yours to delete.

## Children

The app collects no personal data beyond what is described above, so it is
suitable for all ages.

## Changes

If this policy changes, the updated version will be published with the app
listing and the "last updated" date above will change.

## Contact

Questions about this policy: **apps.lucian7977@gmail.com**