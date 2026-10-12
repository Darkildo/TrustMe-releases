<p align="center">
  <img src="assets/logo.png" width="112" alt="TrustMe">
</p>

<h1 align="center">TrustMe</h1>

<p align="center">
  <b>A private messenger with an open server and a trust network.</b><br>
  No phone number. Your account is a key that lives only on your device.
</p>

<p align="center">
  <a href="https://github.com/Darkildo/TrustMe-releases/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/Darkildo/TrustMe-releases?sort=semver"></a>
  <img alt="Platforms" src="https://img.shields.io/badge/Android%20%C2%B7%20iOS%20%C2%B7%20Windows%20%C2%B7%20Linux-1f2a5a">
  <a href="https://github.com/Darkildo/trustme_backend"><img alt="Server source open" src="https://img.shields.io/badge/server%20source-open-2ea44f"></a>
  <a href="README.md"><img alt="Русский" src="https://img.shields.io/badge/lang-%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9-informational"></a>
</p>

---

TrustMe is a messenger for people who want to talk freely without handing their conversations to anyone, including whoever runs the server.
Chat, call, share photos and your location, get together in groups: everything is encrypted right on your device.
And if you would rather not depend even on our server, run your own: its source code is open.

## Download

| Platform | File | Requirements |
| --- | --- | --- |
| **Android** (most phones) | [TrustMe-android-arm64-v8a.apk](https://github.com/Darkildo/TrustMe-releases/releases/latest/download/TrustMe-android-arm64-v8a.apk) | Android 10+ |
| Android, older 32-bit devices | [TrustMe-android-armeabi-v7a.apk](https://github.com/Darkildo/TrustMe-releases/releases/latest/download/TrustMe-android-armeabi-v7a.apk) | Android 10+ |
| Android, not sure which | [TrustMe-android-universal.apk](https://github.com/Darkildo/TrustMe-releases/releases/latest/download/TrustMe-android-universal.apk) | Android 10+, larger file |
| **Windows** | [TrustMe-windows-x64.zip](https://github.com/Darkildo/TrustMe-releases/releases/latest/download/TrustMe-windows-x64.zip) | Windows 10 (19041+) or 11, x64 |
| **Linux**: Ubuntu, Debian, Mint | [TrustMe-linux-x64.deb](https://github.com/Darkildo/TrustMe-releases/releases/latest/download/TrustMe-linux-x64.deb) | Ubuntu 24.04+, Debian 13, Mint 22 |
| Linux, portable | [TrustMe-linux-x64.tar.gz](https://github.com/Darkildo/TrustMe-releases/releases/latest/download/TrustMe-linux-x64.tar.gz) | glibc 2.38+, incl. Fedora 40+ |
| **iOS** | TestFlight, by invitation | iOS 15.6+ |

The links always point to the latest version. Older versions and change notes are in [Releases](https://github.com/Darkildo/TrustMe-releases/releases).

The screenshots show the Russian UI; English is available in settings.

<table>
  <tr>
    <td align="center" width="25%"><img src="assets/screenshots/01-key.png" width="200" alt="Key generation"><br><sub>Your account key is created on the device</sub></td>
    <td align="center" width="25%"><img src="assets/screenshots/02-chat.png" width="200" alt="Chat"><br><sub>End-to-end encrypted chats</sub></td>
    <td align="center" width="25%"><img src="assets/screenshots/03-trust.png" width="200" alt="Contacts by trust"><br><sub>See whom you can trust</sub></td>
    <td align="center" width="25%"><img src="assets/screenshots/04-location.png" width="200" alt="Live location"><br><sub>Location: you decide who and for how long</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="assets/screenshots/05-group.png" width="200" alt="Group"><br><sub>Groups with roles and disappearing messages</sub></td>
    <td align="center"><img src="assets/screenshots/06-call.png" width="200" alt="Call summary"><br><sub>Calls protected by DTLS-SRTP</sub></td>
    <td align="center"><img src="assets/screenshots/07-security.png" width="200" alt="Security"><br><sub>PIN, biometrics and auto-lock</sub></td>
    <td align="center"><img src="assets/screenshots/08-media-encryption.png" width="200" alt="Media encryption"><br><sub>Photos and videos stay encrypted on the phone</sub></td>
  </tr>
</table>

## Why TrustMe

### No phone numbers, no email
To create an account, just swipe across the screen: that motion becomes your key, generated on the device.
You never share a phone number, email or real name, so there is nothing to leak. Add friends by QR code or an invitation code.

### Nobody but the recipient can read your messages
Messages, photos, voice notes, calls and location are encrypted on your device and decrypted only by the recipient.
The server just passes sealed envelopes along. For the most sensitive conversations, turn on forward secrecy:
the key changes with every message, so even a stolen phone cannot reveal what has already been delivered.

### You know who you are talking to
Compare key fingerprints in person and the contact gets a "Verified" mark. Friends can introduce you to each other,
and the app warns you if a contact's key suddenly changes. You decide, contact by contact,
who may call you or see your location and location history.

### Your server, your rules
Use the shared server or run your own for yourself, your family or your team.
[The server's source is open](https://github.com/Darkildo/trustme_backend): a node starts with a single Docker command,
and in the app you only enter its address and key.

### Everything you are used to
This is not a bare-bones "secure chat" but a full messenger: reactions, replies, stickers, voice and round video messages,
polls, groups, video calls and screen sharing from your computer.

## What you can do

**Chat your way.** Reply to specific messages, react, edit and delete for yourself or for everyone.
Record voice messages up to 10 minutes and round video messages, send a batch of photos and videos as one album, touch up a photo in the built-in editor.
Send a secret photo for a single view, or set a conversation to delete itself after an hour, a day or a week.

**Express yourself.** Build your own sticker packs, import them from an archive and share them right in the chat.
Make text bold, italic or hide it under a spoiler. Turn on live typing and your contact sees your reply as you type it
(only if you both want that).

**Call.** Audio and video calls one-to-one and in groups: up to 5 people by voice and up to 3 by video.
Share your computer screen with sound to help with a setup or go through a document together.
On-device noise suppression removes background noise, and on a phone an incoming call takes over the screen like a regular one.

**Meet up.** Share your location with people close to you for 15 minutes, an hour, 8 hours or until you stop.
Contacts you trust can see your location history with stops and routes, and you can export it to GPX.

**Work together.** Create groups with admins and an admins-only posting mode, mention members with @,
run polls with anonymous voting and auto-close. New members see either only new messages or the full history: you choose when creating the group.

**Stay organised.** Search a chat or all chats at once, pin what matters, archive the rest,
keep notes to yourself in Saved Messages. Read receipts and online status are configurable per contact.

**Work on your computer.** Windows and Linux apps with a two-pane layout, tray icon, keyboard shortcuts
and drag and drop. Light and dark themes, Russian and English.

## Openness

- **Server.** [The source code](https://github.com/Darkildo/trustme_backend) is open: the protocol, message schemas and deployment guides are all in the repository.
  You can study it, build it and run your own node; the terms of use are in [LICENSING.md](https://github.com/Darkildo/trustme_backend/blob/master/LICENSING.md).
- **Protocol.** The wire format is described in [server-contract.md](https://github.com/Darkildo/trustme_backend/blob/master/server-contract.md)
  and the [protobuf schemas](https://github.com/Darkildo/trustme_backend/tree/master/schemas). The code lets you check that the server only ever sees encrypted envelopes.
- **The client and the cryptographic core** are being prepared for publication. Until then the app is distributed as ready-made builds from this repository.

## Security and privacy

**Encryption.** Messages, media, location and profile data are encrypted on your device and decrypted only by the recipient:
X25519 key agreement, AES-256-GCM encryption, Ed25519 signatures. Calls use DTLS-SRTP, with signalling over the same encrypted channel.
The connection to the server is additionally protected by the Noise protocol.

**Forward secrecy.** In a direct chat you can turn on an extra Double Ratchet layer: the key changes with every message.
It is enabled per chat and only with both sides' consent. It does not cover groups or calls.

**On the device.**
- Unlock with an 8-digit PIN or a password, plus Face ID, Touch ID or fingerprint.
- Auto-lock after a chosen period; optionally wipe data after 10 failed attempts.
- The local database is encrypted (SQLCipher); the key file is protected with Argon2id and AES-256-GCM.
- Photos, videos and files are stored encrypted on the device (on by default). The keys unlock only after you enter your PIN or password.
- On Android, screenshots are blocked; the app switcher preview is hidden on both mobile platforms.

**Notifications.** The server sends only a wake-up signal, never the content. Your device fetches and decrypts the message and shows the notification itself.

**What the server sees.** The server cannot read message content. It does know who writes to whom, when, and how large each message is, and the shape of your contact graph.
Undelivered messages are kept on the server, encrypted, for up to 14 days. If it matters to you who holds this data, run your own server.

**GIFs and link previews.** GIF search goes through Tenor, so Google sees the query and your IP address. The feature is optional.
Link previews are fetched by the sender's device.

## Backup and transfer

- **Transfer to a new device.** The new device shows a QR code, the old one sends an encrypted file. Keys, contacts and groups move over; no server is involved.
- **Backup.** An encrypted archive protected by a password of at least 12 characters. Restoring from it creates a **new account**: exchange QR codes with your contacts again.
- The backup stays inside the app until you export it. Without a transfer or a backup, losing your device means losing your keys and messages.

## Installation

<details>
<summary><b>Android</b></summary>

1. Download the APK. `arm64-v8a` fits nearly every recent phone; if unsure, take `universal`.
2. Open the file and allow installs from this source when asked.
3. To update, install the new APK over the old one. Messages and keys are kept.

</details>

<details>
<summary><b>Windows</b></summary>

1. Download the zip. Before extracting: right-click → Properties → Unblock (if the checkbox is there).
2. Extract anywhere and run `TrustMe.exe`. There is no installer.
3. The build is not code-signed, so SmartScreen will warn you: More info → Run anyway.
4. To update, replace the whole folder. Data lives separately in `%APPDATA%\com.requiem\TrustMe` and is kept.

Closing the window minimises it to the tray; quit from the tray icon menu. There are no push notifications on desktop: messages arrive while the app is running.
If you see "No connection" with `os error 10013`, allow `TrustMe.exe` network access in your firewall or antivirus.

</details>

<details>
<summary><b>Linux</b></summary>

**.deb** (Ubuntu 24.04+, Debian 13, Mint 22); dependencies are installed automatically:

```sh
sudo apt install ./TrustMe-linux-x64.deb
```

**.tar.gz** (any distribution with glibc 2.38+, including Fedora 40+): extract and run `./TrustMe`.
Install the system libraries yourself:

```sh
# Debian / Ubuntu / Mint
sudo apt install libgtk-3-0t64 libmpv2 libepoxy0 libsecret-1-0 \
     libayatana-appindicator3-1 libpulse0 pulseaudio-utils ffmpeg gnome-keyring
# Fedora
sudo dnf install gtk3 mpv-libs libepoxy libsecret \
     libayatana-appindicator-gtk3 pulseaudio-libs pulseaudio-utils ffmpeg-free gnome-keyring
```

- Keys are stored in the system secret store. Without a running gnome-keyring or KWallet the app will not start and will explain why.
- Screen sharing on Wayland needs xdg-desktop-portal and PipeWire; on X11 it works out of the box.
- Data lives in `~/.local/share/com.requiem.trust_me`; to update the portable build, replace the folder.
- It will not run on Ubuntu 22.04 or other distributions with an older glibc.

</details>

<details>
<summary><b>iOS</b></summary>

iPhone builds are distributed via TestFlight by invitation. iOS 15.6 or later is required.

</details>

## Verifying downloads

Each release includes `SHA256SUMS-android.txt`, `SHA256SUMS-windows.txt` and `SHA256SUMS-linux.txt`.
Compare the checksum of your download with the matching line:

```sh
sha256sum TrustMe-android-arm64-v8a.apk          # Linux
shasum -a 256 TrustMe-android-arm64-v8a.apk      # macOS
```
```powershell
Get-FileHash TrustMe-windows-x64.zip -Algorithm SHA256   # Windows
```

All Android APKs are signed with the same key. If Android refuses to install an update over the installed version, the file was signed with a different key: do not install it.

## Known limitations

- One account works on one device. There is no simultaneous multi-device sync, but the account can be transferred.
- Only received media can be forwarded: text cannot be forwarded, and nothing can be forwarded to groups.
- No push notifications on Windows or Linux.
- No camera video or round video messages on Linux; Windows has both.
- Desktop updates are installed manually.
- Disappearing messages are deleted by the recipient's app; nothing can guarantee the recipient did not save them another way.
- There are no macOS or web builds.

## Reporting a problem

Open an [issue](https://github.com/Darkildo/TrustMe-releases/issues/new/choose) with the app version, your device and the steps that lead to the problem.

> [!WARNING]
> Do not attach diagnostics exports, backups, transfer files or screenshots of conversations: issues are public.
> If logs are needed, you will be asked separately.

Report vulnerabilities privately, not in issues: see [SECURITY.md](SECURITY.md).

## License

The app is free and distributed as ready-made builds from this repository. The server's source is open; its terms are in [LICENSING.md](https://github.com/Darkildo/trustme_backend/blob/master/LICENSING.md).
For anything else: didakostya@gmail.com.
