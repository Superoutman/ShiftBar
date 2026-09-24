# ShiftBar

**English** | [简体中文](README.zh-CN.md)

[![Website](https://img.shields.io/badge/website-shiftbar.0x01.build-687d49)](https://shiftbar.0x01.build)
[![Latest release](https://img.shields.io/github/v/release/Superoutman/ShiftBar?label=download&color=3d9868)](https://github.com/Superoutman/ShiftBar/releases/latest)
[![Designed for macOS 27](https://img.shields.io/badge/requirements-macOS%2027-d99a39)](#installation)
[![Apple Silicon](https://img.shields.io/badge/hardware-Apple%20Silicon-777777)](#installation)

[![Languages](https://img.shields.io/badge/languages-中文%20%7C%20English%20%7C%20日本語-527ca8)](#features)
[![Alpha](https://img.shields.io/badge/status-Alpha-d99a39)](https://github.com/Superoutman/ShiftBar/releases/latest)
[![Apple notarization](https://img.shields.io/badge/notarized-Apple-3d9868)](https://github.com/Superoutman/ShiftBar/releases/latest)
[![GitHub Stars](https://img.shields.io/github/stars/Superoutman/ShiftBar?style=flat&color=9872b3)](https://github.com/Superoutman/ShiftBar/stargazers)
[![Issues](https://img.shields.io/github/issues/Superoutman/ShiftBar?label=issues&color=527ca8)](https://github.com/Superoutman/ShiftBar/issues)

ShiftBar is a companion to **macOS 27's native menu bar folding**, allowing you to choose which icons to hide and expand or collapse them manually.

macOS 27 folds icons when the menu bar runs out of space. You may still want to tuck away less frequently used items while there is room available. ShiftBar adjusts the space available in the menu bar to trigger native folding earlier, so you do not have to wait until the bar fills up.

macOS handles the folding through its native layout. ShiftBar provides control over the hidden range, manual expansion and collapse, and saved settings.

<p align="center">
  <img src="images/menu-bar-demo.png" alt="ShiftBar overview" width="720">
</p>

*ShiftBar overview. Refer to the app for actual behavior.*

## Features

- **Expand and collapse manually:** click the capsule icon in the menu bar to toggle between the two states.
- **Adjust the hidden range:** drag the adjustment bar directly in the menu bar to choose which icons on the left to hide.
- **Hide all icons to the left:** set this from the context menu.
- **Save and restore a backup:** save a separate copy of your hidden range. Further adjustments do not overwrite it; restore it from the menu when needed.
- **Remember settings:** when reopened, the app attempts to restore the last confirmed hidden range.
- **Consistent across displays:** the built-in and external displays keep the same collapsed result.
- **Launch at login:** enable or disable the system login item from the context menu.
- **Three interface languages:** Simplified Chinese, English and Japanese, following macOS language preferences.

ShiftBar stays in the menu bar without a Dock icon. Hiding an icon does not quit its application.

## Installation

Download the `.dmg` installer from [Releases](https://github.com/Superoutman/ShiftBar/releases/latest), move **ShiftBar.app** to **Applications**, and open it.

**Designed for macOS 27.** Requires Apple Silicon (M-series chips). ShiftBar is currently in Alpha.

[Website](https://shiftbar.0x01.build) · [Download](https://github.com/Superoutman/ShiftBar/releases) · [Report an issue](https://github.com/Superoutman/ShiftBar/issues)

## Usage

On first use, allow ShiftBar in **System Settings → Privacy & Security → Accessibility** so it can read menu bar positions and handle range adjustments.

You can postpone the first permission prompt. Later, right-click the menu bar capsule and choose “Open Accessibility Settings…” to continue. ShiftBar detects permission changes automatically without restarting. With no saved position, the capsule starts near the right edge; a one-time guide appears after the first authorization.

1. **Shift-click** the capsule icon to enter range adjustment.
2. Wait for the adjustment bar to be ready, then hold **Shift** and drag: left increases the hidden range; right decreases it.
3. Click the capsule icon to confirm and save the range.

Once configured, click normally to expand the hidden icons, then click again to collapse them.

The context menu provides range adjustment, hiding all icons to the left, saving and restoring the hidden range, and usage instructions. Click the version number at the bottom to check for updates. **About** opens the product website.

## Notes

- The adjustable range depends on screen space, the notch area and the current menu bar layout. The app shows a message when you reach the limit.
- If permissions are unavailable or the layout cannot be confirmed, ShiftBar expands the icons and keeps the previously saved range and backup.
- **Known issue:** Synology Drive is not yet compatible with the current multi-display hiding mechanism. While collapsed, its icon may disappear with the hidden group even when it is inside the intended retained area; expanding ShiftBar restores it.
- The hidden range and backup are stored locally. Menu bar organization works offline and does not require an account.
- The interface follows the order of preferred languages in macOS and supports per-app language settings. It falls back to English when no supported language matches; other Chinese variants use Simplified Chinese. Reopen the app after changing its language.

## Feedback

Use [Issues](https://github.com/Superoutman/ShiftBar/issues) to report problems or suggest improvements. For display, folding or adjustment problems, include your macOS version, ShiftBar version, display setup and steps to reproduce. Add a screenshot or short recording when helpful.
