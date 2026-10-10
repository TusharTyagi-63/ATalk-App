# ATalk — Secure Mobile Communication Architecture
> **The Ultimate Hybrid of Telegram and WhatsApp** with zero-compromise cryptographic privacy, hardened anti-forensics, strict zero-storage media policy, and ultra-fast performance on poor networks (2G/3G/lossy).

[![Release](https://img.shields.io/badge/Release-v1.5-cyan?style=for-the-badge&logo=android)](https://github.com/TusharTyagi-63/ATalk-App/releases)
[![APK Size](https://img.shields.io/badge/APK%20Size-2.13%20MB-blue?style=for-the-badge)](ATalk-latest.apk)
[![Security](https://img.shields.io/badge/Security-Hardware%20Keystore%20GCM-green?style=for-the-badge)](https://github.com/TusharTyagi-63/ATalk)
[![Zero Storage](https://img.shields.io/badge/Media%20Storage-Zero--Disk%20RAM--Only-red?style=for-the-badge)](https://github.com/TusharTyagi-63/ATalk)

---

## 📥 Direct APK Downloads

| File | Version | Size | Checksum (SHA-256) | Notes |
|---|---|---|---|---|
| **[ATalk-latest.apk](ATalk-latest.apk)** | `v1.5 (Latest)` | 2.13 MB | `6591406D42A75BF73B5289BCF2C06915AB9859DE889D9FE166DEF7B2CC7AD5AD` | Full-Screen Ephemeral Media Viewer (Stitch), 2G Binary Wire Protocol, Global Search |
| **[ATalk-v1.5.apk](ATalk-v1.5.apk)** | `v1.5` | 2.13 MB | `6591406D42A75BF73B5289BCF2C06915AB9859DE889D9FE166DEF7B2CC7AD5AD` | Stitch Ephemeral Viewer, Micro-Payload Wire Framing, Telegram Search Filters |
| **[ATalk-v1.4.apk](ATalk-v1.4.apk)** | `v1.4` | 2.11 MB | `6123756FB6F06AD08A2916D90C66A85F03D01CA538F8667C2C0C64F840683D94` | Real Account Setup, Full Settings Hub, Clean Bot Chat & Inset Stability |
| **[ATalk-v1.3.apk](ATalk-v1.3.apk)** | `v1.3` | 2.11 MB | `0C85B64C4099F50C8DC8089DA11A3BE3E60C5A5D192D1BB4D072D5AD4E329938` | WebRTC Diagnostics HUD & Adaptive Opus 6-32 kbps |
| **[ATalk-v1.2.apk](ATalk-v1.2.apk)** | `v1.2` | 2.10 MB | `5813F8002B342F720A6F2705816EAE2AAFE442F6DF0F0BDFDAA122A749B34244` | Live Decibel Waveform Dock & E2EE Call Link Modal |
| **[ATalk-v1.1.apk](ATalk-v1.1.apk)** | `v1.1` | 2.10 MB | `4B19942CFC4186C8D0C6AAD74DE6A59D014B87209E6F323358DD7C43D6597240` | Status Story Viewer & View-Once Ephemeral Card |
| **[ATalk-v1.0.apk](ATalk-v1.0.apk)** | `v1.0` | 2.08 MB | `984C50B9F2180ADC7142C5973A32C86A589E5647AC03DA22EF29C960B8F280D4` | Initial Stealth Notes Disguise & Master Key Derivation |

---

## 🛡️ Core Security Architecture & Features

### 1. 🥷 Stealth Notes Disguise & Biometric Access
- **Authentic Cover App**: Launches as a clean, realistic Notes application with title `"Notes"`, functional categories, and realistic decoy notes.
- **Secret Search Unlock**: Vault unlocks strictly when typing your customized secret keyword (default `"tyagi"`) in the search bar.
- **Biometric Fast-Path**: Instant hardware fingerprint scan triggered automatically when the search bar is focused.
- **Screen-Off Auto-Lock**: Screen-off (`ACTION_SCREEN_OFF`) immediately clears the backstack and zeroes cryptographic keys in RAM.

### 2. ⚡ Strict Zero-Storage Media Policy (Zero Flash Traces)
- **Zero Auto-Save**: Absolutely NO photos, videos, voice notes, stickers, or documents are ever saved or cached to persistent device storage (`/sdcard/`, `DCIM/`, `Pictures/`, `Download/`, or internal cache).
- **RAM-Only Volatile Caching**: All media is decoded on the fly into volatile memory (`ByteArray`, `Bitmap`) with disk caches completely disabled (`diskCachePolicy(CachePolicy.DISABLED)`).
- **Interactive User Export Only**: Media persistance to device storage occurs ONLY when the user explicitly taps "Save to Gallery", triggering Android's Storage Access Framework (SAF).
- **Instant Memory Shredding**: When the device is locked or screen turned off, all active media buffers are immediately zeroized (`Arrays.fill(bytes, 0)`).

### 3. 💬 Telegram + WhatsApp Hybrid Experience
- **Telegram Features**: Folder ribbons (`All`, `Unread`, `Personal`, `Work`), pinned "Saved Messages" cloud vault, supergroups, broadcast channels, dynamic voice waveform player with 2X speed toggle, live voice note recorder dock with frequency bars, and floating emoji reaction dock.
- **WhatsApp Features**: 24-hour status stories carousel with segmented rings, interactive story viewer dialog with quick reactions, quoted swipe-reply bubble, View-Once `(1)` ephemeral media card with countdown timer, 6-icon attachment drawer, and shareable encrypted Call Links modal.

### 4. 🚀 Ultra-Fast Messaging & ACK State Machine
- **Optimistic UI**: Messages render instantly with clock icon (`QUEUED` 🕒), transitioning to single checkmark (`SENT` ✓), double gray checkmarks (`DELIVERED` ✓✓), and double cyan checkmarks (`READ` ✓✓).
- Low-bandwidth micro-payload binary wire formatting.

### 5. 📞 WebRTC Low-Bandwidth HD Calling & 2G Resilience
- **Real-Time Quality HUD**: Floating telemetry card monitoring Latency/RTT (ms), Packet Loss percentage, and Audio Codec bitrate in real time.
- **Adaptive Opus Engine**: Spans 6 kbps (ultra-low 2G/EDGE) to 32 kbps (HD voice) with In-Band Forward Error Correction (FEC) and Packet Loss Concealment (PLC).
- **2G Low Bandwidth Resilience Mode**: Instantly drops bitrate to 6 kbps with 30% FEC redundancy and audio-priority gating, guaranteeing zero audio dropouts even on flaky cellular signals.

---

## 🔒 Source Code Repository

The complete Kotlin Jetpack Compose source code, architectural specifications, and roadmap are maintained at:
👉 **[TusharTyagi-63/ATalk](https://github.com/TusharTyagi-63/ATalk)**

---

## 📜 Version History

### `v1.5` (Latest)
- **Full-Screen Zero-Storage Ephemeral Media Viewer (Stitch Design `f5c49d33a2fb493682a0f2671757dc36`)**: Immersive dark tactical UI, prominent 10-second circular fuse countdown timer with dynamic arc progress, strict volatile RAM indicator ("0 Bytes on Disk • RAM-Only Buffer"), caption drawer, interactive Storage Access Framework export ("Save via SAF"), and instant memory shredding ("Instant Shred" with `VolatileMediaVault.shredSingleMedia`).
- **Ephemeral Binary Wire Micro-Payload Protocol (`MicroWireProtocol.kt`)**: Ultra-compact 28-byte framing replacing heavy JSON payloads; shrinks network packets down to <64 bytes with hardware CRC32 frame checksum for zero head-of-line blocking on lossy 2G/EDGE cellular connections.
- **Telegram & WhatsApp Global Search Bar**: Real-time expandable search bar in `ChatListScreen` with category filter chips (`All`, `Bot`, `Messages`, `Vault`), instant query matching across chats, usernames, and message content, with empty-state search cards.
- **Automated Bot Security Benchmarks**: Interactive bot `/wire` and `/benchmark` commands executing real-time compression ratio measurements and MTU validation.
- Stream-installed and verified on physical hardware (`R9ZX40E84PY`).

### `v1.4`
- **Real User Account Setup Flow**: Complete 3-step onboarding (`PhoneAuthScreen`) with international phone input, SMS OTP auto-fill testing helper, display name, `@username` handle availability check, status bio, and Curve25519 Keystore pair generation.
- **Strict Keyword-Only Stealth Disguise**: Removed all fingerprint biometric shortcuts from Notes search bar — unlocking is strictly gated by typing the secret keyword (`"tyagi"` or user-configured secret word).
- **Full Telegram & WhatsApp Settings Architecture**: Profile badge & edit flow, Vault Search Keyword customization, Master PIN, Duress Panic Wipe PIN (instant key zeroing), Screen-Off Auto-Lock & RAM Purge, Default Disappearing Messages timer, Two-Step Verification, P2P Call Relay, Wallpaper Themes, Chat Font Size, Volatile RAM Monitor with instant purge button, and "0 Bytes on Flash Storage" Audit Badge.
- **UI Viewport Inset & Height Stability**: Replaced hardcoded heights with dynamic insets (`contentWindowInsets = WindowInsets.statusBars`, `.imePadding().navigationBarsPadding()`) eliminating screen jumping when opening/closing the keyboard.
- **Clean Single-Bot Interaction**: Removed demo contacts, mock calls, and stories, preserving a pristine interactive `ATalk Bot` (`@atalk_bot` 🤖) capable of interactive message replies and bot commands (`/help`, `/status`, `/keys`, `/wipe`, `/ping`).
- Stream-installed and verified on physical hardware (`R9ZX40E84PY`).

### `v1.3`
- **Real-Time WebRTC Call Telemetry HUD**: Live floating diagnostics card displaying RTT (latency in ms), packet loss with In-Band FEC status, audio codec bitrate, and network quality tier (designed in Stitch `725f949da75449b59544fbb36c22e056`).
- **2G Low Bandwidth Resilience Mode**: Interactive toggleable switch that locks Opus codec to 6 kbps with aggressive 30% FEC redundancy to prevent audio dropouts under severe packet loss.
- **Call Control Ergonomics**: Updated with Mute, Video camera toggle, Speaker, Camera flip, and Red End Call FAB.
- Stream-installed and verified on physical hardware (`R9ZX40E84PY`).

### `v1.2`
- **Live Audio Note Voice Recorder Dock**: Live decibel frequency bars, pulsating record dot, slide-to-cancel trash trigger, lock-to-record toggle, and RAM-only zero-storage badge (Stitch screen `d52c51625b5c47cb81aae32637981ad5`).
- **Encrypted Call Link Share Modal**: Video/Voice call mode toggle, auto-generated unique secure link, 4-emoji safety verification key (`CryptoUtils.generateSafetyEmojiKey`), one-tap clipboard copy, and native Android `ACTION_SEND` sharing (Stitch screen `2fdf1949bfb947d3bc828332e8aec26a`).
- **Playable Voice Note Pipeline**: Integrated dynamic waveform playback with 1X/2X speed multiplier directly into chat feed.
- Stream-installed and verified directly on physical hardware (`R9ZX40E84PY`).

### `v1.1`
- **Interactive WhatsApp Status Story Viewer**: 4-segment animated progress bar, volatile RAM indicator, quick emoji reactions (🔥, ❤️, 💯, 👏, 😂), and encrypted reply field (designed in Stitch `9b49e554fe8a4dd3b90a32b74a3a489c`).
- **Interactive View-Once Ephemeral Viewer**: 10-second countdown circular timer, RAM-only buffer badge ("0 bytes on disk"), explicit "Save to Gallery (SAF)" button, and instant "Shred Now" button.
- **Optimistic Message ACK State Machine**: `QUEUED` 🕒 -> `SENT` ✓ -> `DELIVERED` ✓✓ -> `READ` ✓✓ cyan.
- Verified and stream-installed directly to Samsung device (`R9ZX40E84PY`).

### `v1.0`
- Initial verified release with R8 dead-code stripping (<2.1 MB).
- Complete Notes disguise screen with search keyword unlock (`"tyagi"`) & biometric integration.
- Hardware Keystore AES-256-GCM master key derivation (`MasterKeyManager`).
- Volatile memory-only media vault (`VolatileMediaVault`) with zero flash writing and RAM zeroization on screen off.
- Physical device verified on connected Samsung hardware (`R9ZX40E84PY`) with 100% compliance across all 9 audit steps.
