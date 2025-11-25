## 📜 Changelog

### Version 2.1.2 (2025-11-24)

**Fixed**
* Resolved a bug preventing the **Force Update** menu item from correctly initiating a scrape cycle.

### Version 2.1.1 (2025-11-24)

**Fixed**
* Synchronized the **Mute** menu item state to prevent "flip-flopping" when toggled.
* Corrected the `Form1` initialization order to prevent duplicate status bars on startup.
* Added the missing `UpdateMuteStatusLabel` helper method.

### Version 2.1.0 (2025-11-24)

**Added**
* **Custom Sound Alerts:** Users can now select a `.wav` file to use instead of the system default beep when a maintenance flag is detected.
* **Sounds Submenu:** Created a dedicated menu to easily switch between "System Default" and "Custom Sound..." options.
* **Version Check:** Implemented asynchronous checking for new releases on application startup.

**Changed**
* Migrated the entire project to the **.NET 8.0** framework for improved performance and stability.
* Refactored timer logic using `try...finally` to ensure the scrape cycle always restarts, preventing infinite update loops.

### Version 2.0.20 (Legacy/Initial Release)

**Changed**
* Initial Public Release.
