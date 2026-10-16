# KP-SUTRA — Downloads

**Krishnamurti Paddhati — Structured Tool for Rule-based Analysis**

KP-SUTRA is a desktop program for KP astrologers. It casts the chart, shows
the KP data, times the event, and checks the chart against the rules of the
KP Handbook. Everything runs on your own computer.

This page holds only the files you install. Open
**[Releases](../../releases/latest)** to download the newest version.

---

## Which file do I download?

Open the newest release. Under **Assets**, take **one** file:

| Your computer | Download this file | What it is |
|---|---|---|
| **Windows 10 / 11** | the file whose name ends in **`Setup.exe`** | The installer. Recommended. |
| **Ubuntu / Linux** | **`KP-SUTRA.AppImage`** | The whole program in one file. |
| Windows, without installing | the file whose name ends in **`Portable.zip`** | Unzip and run. It does **not** update itself. |

You can ignore the other files (`.nupkg`, `.json`, `RELEASES-…`). The program
uses them to update itself.

---

## Windows — install

1. Download the file that ends in **`Setup.exe`**.
2. Double-click it. It installs in one step and asks no questions. It does
   not need administrator (प्रशासक) rights.
3. KP-SUTRA opens by itself. Next time, open it from the **Start menu**.

**"Windows protected your PC".** Windows may show this blue message the first
time. Click **More info**, then **Run anyway**. The message appears because the
installer is not yet signed with a paid certificate. It is not a sign of a
problem with the file.

**"Install Partially Succeeded" or "An Application Control policy has blocked
this file".** This is **Smart App Control**, a guard switched on in some new
Windows 11 computers. It blocks programs that Microsoft does not know yet, and
it has no "Run anyway" button. To use KP-SUTRA:

1. Open **Windows Security → App & browser control → Smart App Control
   settings**, and choose **Off**.
2. Run the Setup file again and choose **Repair**.

KP-SUTRA is installed in your own profile folder:
`%LocalAppData%\KP-SUTRA`

## Ubuntu / Linux — install

1. Download **`KP-SUTRA.AppImage`**. Keep it in a folder of your choice, for
   example your home folder.
2. Make it runnable, once. Either right-click it → **Properties** →
   **Allow executing file as program**, or run:

   ```bash
   chmod +x KP-SUTRA.AppImage
   ```

3. Double-click it to open KP-SUTRA.

**If it does not open and the message mentions "FUSE"**, install one small
package, then try again:

```bash
sudo apt install libfuse2t64     # Ubuntu 24.04 and newer
sudo apt install libfuse2        # Ubuntu 22.04
```

**A menu entry (optional).** An AppImage does not add itself to the
applications menu. The free tool
[AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher) can do
that for you.

---

## Updates

You install KP-SUTRA **once**. After that it keeps itself up to date.

- A few seconds after KP-SUTRA starts, it checks for a new version. It says
  nothing unless one exists.
- When a new version exists, it asks you. Click **Update now** to download it.
- Only the **changed parts** are downloaded. A small fix is usually less than
  a few MB.
- Choose **Restart now** to install at once, or **Later** to install it the next
  time you close KP-SUTRA.
- You can also check at any time: **Help → Check for Updates**.

Your charts and settings are kept as they are. You never need a new folder.

The checking needs the internet. Everything else in KP-SUTRA works offline.

---

## Your charts are safe

Your own data is **not** stored inside the program. Installing, updating or
uninstalling KP-SUTRA never touches it.

| Computer | Where your charts, analyses and settings are kept |
|---|---|
| Windows | `%APPDATA%\KPAnalysis\KP-SUTRA\userdata.db` |
| Ubuntu / Linux | `~/.local/share/KPAnalysis/KP-SUTRA/userdata.db` |

**Make a backup now and then.** Copy that folder to a USB drive or another
safe place. To move to a new computer, copy the folder to the same place there
before you first open KP-SUTRA.

---

## Moving from an older unzipped version

Earlier versions came as a zip folder. You can move to the installed version
like this:

- **You used v0.6.9a.** Your charts are already in the folder above. Install
  the new version, open it, and check that your charts are there. Then delete
  the old unzipped folder.
- **You used v0.6.9 or older.** Do this **before** you open the new version for
  the first time:
  1. In your old KP-SUTRA folder, find the file `kpdata.db`. It is in `data`
     or in `_internal\data`.
  2. Copy it into the folder from the table above
     (`%APPDATA%\KPAnalysis\KP-SUTRA` on Windows). Create the folder if it
     does not exist.
  3. Rename the copy to **`kpdata_old.db`**.
  4. Install and open the new version. It brings your charts across by
     itself.

  **Opened the new version first?** It then starts with two sample charts,
  and your old charts are not brought across. Close KP-SUTRA, rename
  `userdata.db` in that folder to `userdata_unused.db`, do steps 1–3, and open
  KP-SUTRA again.

  Keep the old folder until you have checked your charts.

---

## Uninstall

- **Windows:** **Settings → Apps → Installed apps → KP-SUTRA → Uninstall.**
- **Ubuntu / Linux:** delete the `KP-SUTRA.AppImage` file.

Your charts stay in their folder (see above). Delete that folder too only if
you really want to remove them.

---

## Test versions

Some releases are marked **Pre-release**. Those are test builds, for example
`0.6.9b`. Use them only if you were asked to test. A normal installation never
receives a test build. It updates only to normal releases.

---

## What you need

| | |
|---|---|
| Windows | Windows 10 or 11, 64-bit |
| Linux | Ubuntu 22.04 or newer, 64-bit (other modern Linux systems usually work) |
| Memory | 4 GB (8 GB is more comfortable) |
| Disk space | About 1.5 GB — the program, plus one update package it keeps for the next update |
| Screen | 1024 × 768 or larger |

---

## If something goes wrong

KP-SUTRA writes a log file. Please send it along with a short note of what you
did.

| Computer | Log folder |
|---|---|
| Windows | `%APPDATA%\KPAnalysisApp\logs\` |
| Ubuntu / Linux | `~/.local/share/KPAnalysisApp/logs/` |

The file `kp_app.log` is the main log. If KP-SUTRA could not start at all,
there is also a `crash.log` in the same folder.

To report a problem, open the **Issues** tab of this page.

---

## मराठीत थोडक्यात

- **Windows:** `Setup.exe` ने संपणारी फाईल डाउनलोड करा आणि दोनदा क्लिक करा. एकदाच
  install करायचे आहे.
- **Ubuntu:** `KP-SUTRA.AppImage` डाउनलोड करा, एकदा `chmod +x KP-SUTRA.AppImage`
  करा, आणि उघडा.
- **Update:** नवीन आवृत्ती आली की KP-SUTRA स्वतः विचारते. **Update now** दाबा. फक्त
  बदललेला भागच डाउनलोड होतो.
- **तुमच्या पत्रिका सुरक्षित आहेत.** त्या program च्या बाहेर, तुमच्या स्वतःच्या
  folder मध्ये ठेवल्या जातात. Update किंवा uninstall केल्याने त्या जात नाहीत.
- वेळोवेळी त्या folder ची backup घ्या.

---

## Licence

KP-SUTRA is released under the **GNU AGPL-3.0** licence. Planet positions come
from NASA's JPL DE440 data. The program's screens use Qt for Python (PySide6),
under the LGPL-3.0 licence.
