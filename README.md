# ASOS Monitor

[](https://www.google.com/search?q=https://github.com/tactical-taco/ASOS-Monitor/releases/latest)
[](https://dotnet.microsoft.com/download/dotnet/8.0)

A lightweight, dedicated Windows Forms application built on **.NET 8.0** to continuously monitor the METAR (Aviation Routine Weather Report) status of critical ASOS/AWOS stations. This tool is specifically designed to alert the user immediately when an instrument maintenance flag (`.` or `$`) appears in the report.

-----

## ✨ Key Features

  * **Continuous Monitoring:** Scrapes data from the Aviation Weather API at user-defined intervals (5, 10, 15, 30, or 60 minutes).
  * **Stale Data Warning:** Checks the observation time within the METAR. If the report is **older than 60 minutes**, the station status will display **"Data Old"** with the last reported time.
  * **Maintenance Alerts:** Visually flags stations with "Maintenance Required" (`.`) or "Maintenance Flag" (`$`) and plays an audible notification.
  * **Custom Sound Alerts:** Easily switch between the system default sound and a custom user-defined **WAV file** for notifications.
  * **Stability:** Robust error handling prevents crashes and ensures the monitoring timer resets reliably after network failures or exceptions.
  * **Site Management:** Tools for bulk site ID addition, removal, and versatile import/export of monitoring lists.
  * **Update Checker:** Notifies the user on startup if a newer version of the application is available on the GitHub repository.

-----

## ⚙️ Installation & Usage

1.  **Download:** Download the latest release from the [Releases page](https://www.google.com/search?q=https://github.com/tactical-taco/ASOS-Monitor/releases/latest).
2.  **Unzip:** Extract the contents of the downloaded ZIP file to a location on your computer.
3.  **Run:** Execute `ASOSMonitor.exe`. No installation or external dependencies (beyond Windows itself) are required.

The application will start immediately, displaying the status of any loaded sites.

-----

## 📝 Site Management (Import & Export)

Sites are monitored using their **four-letter ICAO identifier** (e.g., `KLAX`, `KMIA`, `KDFW`).

### Adding Sites

1.  Go to **File** \> **Add Site(s)**.
2.  You can enter a single site ID or paste a bulk list, separated by new lines or commas.

### Exporting Sites

  * Go to **File** \> **Export Sites**.
  * This creates a **`sites.json`** file in the standardized **ASOS Monitor 2.0** format, which can be used for backup or sharing.

### Importing Sites

  * Go to **File** \> **Import Sites**.
  * You will be presented with two options:
      * **ASOS Monitor 2.0:** Imports site lists saved in the current `.json` format.
      * **ASOS Monitor 1.0:** Provides backwards compatibility for importing site lists from the older, legacy format.

-----

## 🔔 Options & Settings

All settings are available under the **Options** menu:

| Menu Item | Function |
| :--- | :--- |
| **Sounds** \> **System Default** | Instantly reverts the notification sound to the standard Windows beep. |
| **Sounds** \> **Custom Sound...** | Opens a dialogue to select a specific `.wav` file for alerts. |
| **Mute** | Toggles audible notifications ON/OFF. The status bar will show "🔇 Muted" when active. |
| **Always on Top** | Keeps the application window visible over all other windows. |
| **Update Frequency** | Sets the interval (5, 10, 15, 30, or 60 minutes) for data scraping. |

-----

## 📜 Changelog

### Version 2.1.3 (New Feature\!)

**Added**

  * **Stale Data Warning:** Implemented a check to determine if a METAR report is older than 60 minutes, displaying the last known observation time when data is old.

### Version 2.1.2

**Fixed**

  * Resolved a bug preventing the **Force Update** menu item from correctly initiating a scrape cycle.

### Version 2.1.1

**Fixed**

  * Synchronized the **Mute** menu item state to prevent "flip-flopping" when toggled.
  * Corrected the `Form1` initialization order to prevent a duplicate status bar on startup.
  * Ensured that a blank API response (e.g., for a non-existent station) correctly displays **"Data Unavailable."**

### Version 2.1.0

**Added**

  * **Custom Sound Alerts:** Users can now select a `.wav` file for maintenance flag notifications.
  * **Sounds Submenu:** Created a dedicated menu to easily switch between "System Default" and "Custom Sound..." options.
  * **Version Check:** Implemented asynchronous checking for new releases on application startup.
  * **Error Resilience:** Added robust `try...finally` blocks to the scraper timer to guarantee continuous operation and prevent infinite update loops following network errors.

**Changed**

  * Migrated the entire project to the **.NET 8.0** framework.

-----

## 💻 Built With

  * C\#
  * .NET 8.0 (Windows Forms Application)
  * Visual Studio

-----

## 🤝 Contribution

Feel free to open issues for bugs or suggest new features\!

-----

### 💖 Support the Project
This app is a passion project built in my spare time. If you find the **ASOS Monitor** useful and want to show your appreciation, you can literally [buy me a coffee](https://buymeacoffee.com/ke5wydf)! Your support helps keep me fueled for bug fixes and new features.

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Donate-orange?style=flat&logo=buy-me-a-coffee)](https://buymeacoffee.com/ke5wydf)
