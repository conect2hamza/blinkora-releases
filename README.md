# Blinkora

> Rest your eyes. Move more.

Blinkora is a free, private break reminder for Windows and Mac. Every 20 minutes of _active_ work it asks you to rest your eyes. Every hour it gets you up for a short walk, and every 90 minutes it reminds you to drink water. It never interrupts while you're away, in a call, presenting, in a fullscreen app or outside your work hours, and all of its data stays on your computer.

**[⬇ Download the latest version](https://github.com/conect2hamza/blinkora-releases/releases/latest)** for Windows 10/11 or macOS 10.15+.

![Eye break screen](docs/screenshots/features/break-eye.png)

## Contents

- [Who it's for](#who-its-for)
- [Features](#features)
- [Screenshots](#screenshots)
- [Install](#install)
- [Using Blinkora](#using-blinkora)
- [Updates and uninstall](#updates-and-uninstall)
- [Privacy](#privacy)
- [Troubleshooting](#troubleshooting)
- [Known limitations](#known-limitations)

## Who it's for

People who spend hours at a computer and end up with tired eyes, sitting too long and forgetting to drink. Blinkora gives short, regular breaks that fit around real work instead of fighting it.

## Features

- **Three break types:**
  - Eye break: 30 s every 20 min.
  - Walk break: 2 min every hour.
  - Water break: 2 min every 90 min.
  - Each has its own simple animation, and all of them are adjustable. Presets: Gentle, Balanced and Strict.
- **Counts active time only.** Time away from the keyboard doesn't count, and a long absence counts as a break.
- **Smart pause.** Breaks wait while you're in a call, presenting, or using a fullscreen app, game or video, or one of your chosen "ignored" apps.
- **Heads-up first.** A small card appears before each break, with Start now and Postpone.
- **Work hours.** Silent outside them; different hours per day and overnight shifts are supported.
- **Tray icon.** Live timers, take a break now, and pause for 30 min, 1 hour or until tomorrow.
- **Dashboard.**
  - Today's breaks, active time and streak.
  - 7- and 30-day stats.
  - Every setting.
- **Looks and language.** Light and dark themes, 9 colour themes, English and Roman Urdu.
- **Privacy first.** Local data only, export or delete it any time; the only network use is the update check.
- **Updates.** Automatic on Windows, plus a "Check for updates" popup that lists what's new.

## Screenshots

Taken from the running app (Windows 11).

| Today                                          | Tray                                                |
| ---------------------------------------------- | --------------------------------------------------- |
| ![Today](docs/screenshots/dashboard/today.png) | ![Tray popover](docs/screenshots/features/tray.png) |

| Walk break                                              | Water break                                               |
| ------------------------------------------------------- | --------------------------------------------------------- |
| ![Walk break](docs/screenshots/features/break-walk.png) | ![Water break](docs/screenshots/features/break-water.png) |

| Pick a rhythm                                                        | Breaks settings                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------- |
| ![Setup: rhythm](docs/screenshots/workflows/onboarding-2-rhythm.png) | ![Breaks settings](docs/screenshots/settings/breaks.png) |

More in the [user guide](docs/USER_GUIDE.md).

## Install

|          | Windows                            | Mac                                                   |
| -------- | ---------------------------------- | ----------------------------------------------------- |
| Requires | Windows 10 or 11, 64-bit           | macOS 10.15 Catalina or later, Intel or Apple Silicon |
| Download | `Blinkora_<version>_x64-setup.exe` | `Blinkora_<version>_universal.dmg`                    |
| Status   | Tested                             | Built, not yet tested on a real Mac                   |

Get them from the **[latest release](https://github.com/conect2hamza/blinkora-releases/releases/latest)** on this repository.

**Windows:** run the setup file. No admin rights are needed; it installs for your user account only. If Windows SmartScreen appears, click **More info → Run anyway**, because the installer isn't code-signed yet.

**Mac:** open the `.dmg` and drag Blinkora to Applications. The first time, right-click Blinkora → **Open → Open**. On macOS 15+, use **System Settings → Privacy & Security → Open Anyway**.

On first start, a short setup asks for your theme, break rhythm, work hours and whether to start at login.

## Using Blinkora

- **Find it:** Blinkora runs in the system tray (the menu bar on Mac). Click the icon for timers, pause and _Take a break now_; right-click for a menu.
- **When a break comes:**
  - A heads-up card appears first (Start now / Postpone 5 min).
  - The break screen then covers every monitor, with Postpone 1 min and Skip (or **Esc**).
- **Settings:** open the dashboard from the tray to see your stats and change any setting.
- **Background:** closing the dashboard doesn't stop Blinkora. Use **Quit** in the tray to stop it.
- **Shortcut:** **Ctrl+Alt+B** (Mac: Cmd+Alt+B) takes a break now.

Full step-by-step guide with all settings: **[docs/USER_GUIDE.md](docs/USER_GUIDE.md)**.

## Updates and uninstall

- **Updates (Windows):** Blinkora checks for updates every 6 hours and offers **Install & restart**. To check now, use **Check for updates** in the dashboard sidebar; the popup shows what's new.
- **Updates (Mac):** download the new `.dmg` from the Releases page.
- **Uninstall (Windows):** Settings → Apps → Installed apps → Blinkora → Uninstall. Delete `%APPDATA%\com.blinkora.app` too if you also want to remove your history.
- **Uninstall (Mac):** move Blinkora to the Bin. Delete `~/Library/Application Support/com.blinkora.app` to remove your history.

## Privacy

- **Never read:** what you type, mouse position, window titles, websites, clipboard or audio. The microphone check only asks whether _any_ app is using the mic.
- **Break background (Windows):** the blurred image lives in memory for the length of a break and is never written to disk.
- **Stored on your computer:** break history (kept 90 days), active seconds per minute (kept 30 days) and your settings. Nothing else.
- **No account, no cloud, no analytics.** The only network request is the optional update check against GitHub, and updates are installed only if their signature matches.
- **Your data:** export or delete it from **Privacy & data**.

## Troubleshooting

| Problem                                           | What to do                                                                                                                                                |
| ------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Windows protected your PC"                       | Click **More info → Run anyway** (the installer isn't code-signed yet).                                                                                   |
| Mac says the app can't be opened                  | Right-click → **Open → Open**, or **Privacy & Security → Open Anyway**.                                                                                   |
| A break didn't come when expected                 | Only active work time counts, and breaks wait during calls, fullscreen apps and outside work hours. The tray shows the time left.                         |
| Doesn't start at login although the setting is on | Update to the latest version, which repairs a missing login entry at start. On older versions, turn **Start at login** off and on again under **Breaks**. |
| A break screen won't close                        | Press **Esc** or **Skip**; if that fails, **Quit** from the tray and restart.                                                                             |

More answers in the [user guide](docs/USER_GUIDE.md#troubleshooting-and-faq).

## Known limitations

- **Unsigned installers:** Windows and macOS warn on first install.
- **Mac version:** not yet tested on a real Mac, and it doesn't update itself yet.
- **No licence chosen yet.**
