# ChudStream

<p align="center">
  <strong>A unified, high-performance CloudStream experience for Phone, Tablet and Android TV</strong>
</p>

<p align="center">
  <a href="https://github.com/ChudForks/ChudStream-Releases/releases/latest"><img src="https://img.shields.io/github/v/release/ChudForks/ChudStream-Releases?style=for-the-badge&color=blue&label=Stable%20Release" alt="Stable Release"></a>
  <a href="https://github.com/ChudForks/ChudStream-Releases/releases"><img src="https://img.shields.io/github/v/release/ChudForks/ChudStream-Releases?include_prereleases&style=for-the-badge&color=red&label=Beta%20Release" alt="Beta Release"></a>
  <a href="https://developer.android.com/"><img src="https://img.shields.io/badge/Platform-Android%205.0%2B-green?style=for-the-badge&logo=android" alt="Platform"></a>
</p>

---

**ChudStream** is an enhanced, independent fork of [CloudStream 3](https://github.com/recloudstream/cloudstream). It solves common pain points of multi-provider streaming—such as fragmented search results, lost watch progress across providers, intrusive Cloudflare challenges, and clunky TV player controls—while retaining CloudStream's modular architecture.

---

> [!IMPORTANT]
> ### 📜 Source Code Availability
> **ChudStream source code is available upon request!**  
> If you would like to inspect, audit, or build the source code yourself, simply request it from the maintainer, and the complete source code will be provided.

---

## ⚡ What Makes ChudStream Different?

### 🎯 1. Unified Multi-Provider Streaming Engine
In standard CloudStream, searching for a show returns separate cards for every provider, and switching providers requires backing out to main search. **ChudStream unifies providers into a single seamless interface**:
- **Grouped Search Grid**: Search results from different providers are automatically deduplicated and combined into a single flat card.
- **Direct Show Navigation**: Tap any card to open its details page immediately without pre-load modal popups.
- **In-Player Provider Switching**: Switch between matching providers on-the-fly directly inside the player settings deck without losing playback position.
- **Automatic Fallback & Failover**: If a selected provider has no playable links or fails during stream initialization, ChudStream automatically cycles through alternative matched providers behind the scenes.
- **In-Player Refresh**: Manually refresh alternative sources inside the player at any time with a single click.
- **Smart Provider Matcher**: Prevents movie spin-offs (e.g. *"Movie 1"*) from polluting series episode provider listings.
- **One-Shot Cloudflare Pre-Warming**: Pre-seeds Cloudflare/DDoS-Guard cookies in the background on your first show click so playback is never interrupted by WebView challenges.

### 🔄 2. Universal Watch Progress & Library Sync
- **Cross-Provider Resume**: Watch progress (timestamps) and episode watch states sync across all matching providers of the same show.
- **Deduplicated Feeds**: *Continue Watching* and *Bookmarks* rows on the Home screen collapse duplicates so each title appears exactly once.
- **Decoupled Library & Watch Status**: Adding a title to your library (+ Add to Library) is independent from setting its watch status (*Watching*, *Completed*, *On Hold*, etc.). Titles with no status assigned remain fully visible in your local Library.

### 🎬 3. YouTube-Style Modern Video Player
- **YouTube Red Progress Bar**: High-contrast played track (`#FF0000`) with smooth thumb scrubbing.
- **Grouped Monospace Timestamps**: Clean `00:00 / 00:00` current and remaining duration layout on the bottom-left.
- **Floating Controls Deck**: Borderless floating controls layered transparently over the video.
- **Top-Right Settings Cog**: Replaces bottom menu clutter with a clean, centralized settings popup (Aspect Ratio, Speeds, Captions, Audio/Subtitle Sync, Lock Screen).
- **Out-of-the-Box Double Tap to Seek**: Fast-forward (10s) and rewind (10s) with responsive left/right double taps.

### 📺 4. Tailored Android TV & Big-Screen Controls
- **3x2 Category Grid Settings Hub**: A lightweight, D-pad optimized settings interface designed for low-power devices like Amazon Fire TV sticks and Android TV boxes.
- **Unified TV In-Player Settings Deck**: A single, elegant D-pad friendly settings surface replacing nested dialogs.
- **Fine Seekbar Precision**: TV arrow keys scrub with a 1-second base step and gentle acceleration curve (`1s → 2s → 4s → 8s → 15s → 30s`), with real-time visual timestamp feedback and zero playback stutter.
- **High-Speed Fast Forward (2x to 16x)**: Cycle speeds up to 16x smoothly with automatic audio muting at 4x+ to prevent ExoPlayer buffer underruns.
- **Automated Skip Intro Pill**: A focusable TV capsule pill floating above the seekbar whenever intro timestamps are detected.

### 🛠️ 5. English-First & Ethical Safety Filter
- **Pre-Seeded Extension Repos**: Comes pre-loaded with top repositories (Hexated, MegaRepo, Phisher Repo, CXXX, GizliKeyif) so you don't start with an empty app.
- **Streamlined Setup Wizard**: Skips redundant language selection screens and takes you straight to extension and layout configuration.
- **Ethical NSFW Plugin Blocklist**: Built-in filter automatically blocks extensions known to host non-consensual, deepfake, or illegal content across all repositories.

---

## 📊 Feature Comparison: ChudStream vs. Standard CloudStream 3

| Feature | Standard CloudStream 3 | ChudStream |
| :--- | :---: | :---: |
| **Search Grid** | Per-provider duplicate rows | **Unified deduplicated grid cards** |
| **Provider Source Switcher** | Return to search | **In-player dynamic source swap** |
| **Stream Failure Recovery** | "No links found" error | **Automatic provider failover cycling** |
| **Watch Progress Sync** | Locked to specific provider | **Universal across all providers** |
| **Player UI Style** | Legacy Android player controls | **YouTube-style minimalist layout** |
| **TV Settings Interface** | Standard mobile preference tree | **3x2 Category Grid Hub** |
| **TV Player Settings** | Stacked modal dialogs | **Unified D-Pad Glass Deck** |
| **TV Seekbar Precision** | Fixed 30s chunk jumps | **1s precision + dynamic acceleration** |
| **TV Fast-Forward Speeds** | Basic 1.0x / 2.0x | **2x, 3x, 4x, 8x, 16x + Auto-Mute** |
| **Library Membership** | Tied to Watch Status | **Decoupled independent library state** |
| **Cloudflare Bypass** | Mid-stream popup interruption | **One-Shot background pre-warming** |
| **Pre-loaded Repositories** | Basic default list | **Hexated, MegaRepo, Phisher + 18+ repos** |
| **NSFW Safety Filter** | None | **Precautionary ethical blocklist** |

---

## 📥 Download & Release Channels

ChudStream is available in two official release channels:

| Channel | Best For | Description |
| :--- | :--- | :--- |
| 🟢 **[Stable Channel](https://github.com/ChudForks/ChudStream-Releases/releases/latest)** | Everyday Viewing | Thoroughly tested milestone builds. Download `ChudStream-stable.apk`. |
| 🔴 **[Prerelease / Beta](https://github.com/ChudForks/ChudStream-Releases/releases)** | Cutting-Edge Features | Automated builds from the latest code changes. Download `ChudStream-prerelease-debug.apk`. |

> [!NOTE]
> ### 🔑 Persistent Signing Key Notice (v1.1.1+)
> Starting in **Version 1.1.1**, ChudStream uses a permanent release signing certificate.  
> If you are updating from an older ChudStream build (prior to v1.1.1), **uninstall the existing app once**, then install the new APK. All future updates within the same channel will update seamlessly in-place.

---

## 🚀 How to Install & Use

1. **Download**: Grab the latest `.apk` from the [Releases](https://github.com/ChudForks/ChudStream-Releases/releases) page on your device or Fire TV.
2. **Install**: Open the downloaded file and allow installation from unknown sources if prompted.
3. **First-Run Setup**:
   - Complete the brief setup wizard (select your preferred layout: **Phone** or **TV**).
   - Browse the pre-loaded **Extension Repositories** and install your desired stream providers.
4. **Enjoy**: Search any movie or show—ChudStream will group matching providers into a single card!

---

## 🔒 Security & Release Integrity

- All APKs published in this repository are compiled and signed automatically via GitHub Actions workflows.
- ChudStream includes built-in auto-updater checks to notify you of new releases directly inside the application.

---

## 📄 Requesting Source Code

As noted above, ChudStream's source repository is privately maintained, but **anyone is welcome to request the full source code**.  
If you would like to inspect, modify, or compile the codebase, please open an issue in this repository or contact the maintainer directly, and the complete source code will be provided.

---

<p align="center">
  <em>ChudStream is an independent community fork and is not officially affiliated with or endorsed by CloudStream 3.</em>
</p>
