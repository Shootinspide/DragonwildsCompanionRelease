# Dragonwilds Companion 3.0.0

Version 3.0.0 adds the first native Android companion and the secure desktop
relay it uses for live RuneScape: Dragonwilds data. Content and compatibility
are current for Dragonwilds 1.0.1.

## Native Android app

- Live skill levels, total XP, XP to next level, session XP and XP per minute.
- Native high-resolution Ashenfall map with pan, pinch zoom, 9,173 locations,
  38 toggleable filters, marker details, objective highlights and a live player
  direction marker.
- Custom base, chest, farming and unfinished-activity pins plus route drawing.
- Full quest, activity, vault, boss and achievement journal with 82 entries.
- Offline map, filters, pins and journal progress; objective changes queue safely
  until the encrypted PC connection returns.
- RuneScape-inspired dark teal, gold and parchment interface using the game's
  skill icons.

## Secure live connection

- Explicitly opt-in desktop relay that binds only to the private IPv4 adapter
  selected by the player.
- Ten-digit, single-use pairing code with a five-minute lifetime.
- AES-256-GCM authenticated encryption with per-device keys, replay protection
  and device revocation.
- Android keys use SecureStorage; desktop copies use Windows data protection.
- No save files, Steam IDs, Windows paths, character names, passwords or account
  credentials are transmitted to the phone.

## Desktop improvements

- New **Mobile App Connection** screen for enabling the relay, choosing the
  adapter, pairing phones and revoking devices.
- Dragonwilds 1.0.1 journal and map catalogue compatibility.
- Long-lived mobile sessions, atomic paged journal synchronization and safer
  recovery of malformed local journal files.
- Update redirects remain restricted to the signed channel's exact host list.

## Install

1. Install `Dragonwilds.Companion.Setup.exe` on the gaming PC.
2. Install `Dragonwilds.Companion.Android.apk` on an Android phone.
3. In the desktop companion, open **Mobile App Connection**, select the private
   Wi-Fi adapter, enable the bridge and create a pairing code.
4. On the phone, enter the displayed IP address, port and one-time code.

Both devices must be on the same private Wi-Fi for live updates. The Android
app remains useful offline for the map and journal. This release does not ship
an iPhone package because Apple requires the final iOS build to be signed on a
Mac with Xcode.

This is an independent, non-commercial fan project and is not affiliated with
or endorsed by Jagex.
