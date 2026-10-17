# Delete your CarHA data

_Last updated: 17 October 2026_

CarHA does not have a user account, and we do not operate any server. Everything
you configure is stored only in the app's private storage **on your own phone**.
Nothing is uploaded to us, so there is nothing for us to delete on your behalf —
you delete it directly, immediately, and completely.

## How to delete your data

You can use any of these three methods. All of them are immediate.

### 1. Delete individual items inside the app

- **Settings** → tap the trash icon next to a service (Home Assistant, MQTT,
  eWeLink, Tuya, Shelly) to remove that account and its credentials.
- **Tabs** → open a tab → delete buttons, or delete the whole tab.
- **Geofence** → tap the trash icon on a zone. This also unregisters the system
  geofences for that zone.

### 2. Delete everything at once (recommended)

1. Open **Android Settings**
2. **Apps** → **CarHA**
3. **Storage & cache** → **Delete application data** (or "Clear storage")

This erases every service credential, tab, button, geofence zone and preference
stored by the app on your device.

### 3. Uninstall the app

Long-press the CarHA icon → **Uninstall**. Android removes all app data with it.

## What is deleted

- Service credentials: Home Assistant URL and long-lived token, MQTT
  host/port/username/password, eWeLink email and password, Tuya user code and
  tokens, Shelly authorization key and server URI
- Your tabs, button names, entity IDs, icons, colours and ordering
- Geofence zones: name, coordinates, radii, actions and notification message
- The "voice confirmation" preference

## What is *not* stored anywhere

CarHA keeps no backup on any server of ours, has no analytics, and has no
account system. Uninstalling or clearing the data is final — there is no
residual copy.

If you exported a backup file (More → Export), that file was written to a
location **you** chose on your device or in your own cloud storage. You delete
it the same way you delete any other file.

## Deletion of data held by the services you connected

CarHA is only a client for services you configured yourself. To delete data
held by those providers, use their own account settings:

- **Home Assistant** — your own server, so you control the data directly
- **eWeLink / Sonoff** — eWeLink account settings
- **Tuya / Smart Life** — Tuya account settings
- **Shelly** — Shelly Cloud account settings

## Contact

If you have any question about deletion, email
**apps.lucian7977@gmail.com** and we will answer within 30 days.