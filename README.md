# ATalk — Secure Mobile Communication Architecture
> **The Ultimate Hybrid of Telegram and WhatsApp** with zero-compromise cryptographic privacy, hardened anti-forensics, strict zero-storage media policy, and ultra-fast performance on poor networks (2G/3G/lossy).

[![Release](https://img.shields.io/badge/Release-v1.0-cyan?style=for-the-badge&logo=android)](https://github.com/TusharTyagi-63/ATalk-App/releases)
[![APK Size](https://img.shields.io/badge/APK%20Size-2.08%20MB-blue?style=for-the-badge)](ATalk-latest.apk)
[![Security](https://img.shields.io/badge/Security-Hardware%20Keystore%20GCM-green?style=for-the-badge)](https://github.com/TusharTyagi-63/ATalk)
[![Zero Storage](https://img.shields.io/badge/Media%20Storage-Zero--Disk%20RAM--Only-red?style=for-the-badge)](https://github.com/TusharTyagi-63/ATalk)

---

## 📥 Direct APK Download

| File | Version | Size | Checksum (SHA-256) |
|---|---|---|---|
| **[ATalk-latest.apk](ATalk-latest.apk)** | `v1.0 (Latest)` | 2.08 MB | `984C50B9F2180ADC7142C5973A32C86A589E5647AC03DA22EF29C960B8F280D4` |
| **[ATalk-v1.0.apk](ATalk-v1.0.apk)** | `v1.0` | 2.08 MB | `984C50B9F2180ADC7142C5973A32C86A589E5647AC03DA22EF29C960B8F280D4` |

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
- **Telegram Features**: Folder ribbons (`All`, `Unread`, `Personal`, `Work`), pinned "Saved Messages" cloud vault, supergroups, broadcast channels, dynamic voice waveform player with 2X speed toggle, and floating emoji reaction dock.
- **WhatsApp Features**: 24-hour status stories carousel with segmented rings, quoted swipe-reply bubble, View-Once `(1)` ephemeral media card, 6-icon attachment drawer, and shareable encrypted Call Links.

### 4. 📞 Low-Network HD Calling & Messaging
- Tuned for low-bandwidth 2G/3G networks, surviving up to 30% packet loss with adaptive Opus audio (6–32 kbps) with In-Band FEC and PLC.
- Hardware acoustic echo cancellation (AEC) and noise suppression (NS).
- Ultra-compact binary wire payloads minimizing cellular byte consumption.

---

## 🔒 Source Code Repository

The complete Kotlin Jetpack Compose source code, architectural specifications, and roadmap are maintained at:
👉 **[TusharTyagi-63/ATalk](https://github.com/TusharTyagi-63/ATalk)**

---

## 📜 Version History

### `v1.0` (Latest)
- Initial verified release with R8 dead-code stripping (<2.1 MB).
- Complete Notes disguise screen with search keyword unlock (`"tyagi"`) & biometric integration.
- Hardware Keystore AES-256-GCM master key derivation (`MasterKeyManager`).
- Volatile memory-only media vault (`VolatileMediaVault`) with zero flash writing and RAM zeroization on screen off.
- Physical device verified on connected Samsung hardware (`R9ZX40E84PY`) with 100% compliance across all 9 audit steps.
