# Office LTSC 2024 for macOS — Installation Guide

> **Activation Method:** VL Serializer (primary) — required on Mac even if you have a KMS server.
> **KMS Server:** `kms.danipras.dev:1688` — for Windows machines only. See [KMS section](#kms-activation-windows-only) for details.

---

## System Compatibility

| macOS Version | Installer to Use |
| --- | --- |
| macOS 14 (Sonoma) or later | Office LTSC 2021/2024 v16.107.1 |
| macOS 13 (Ventura) | Office LTSC 2021/2024 v16.101 |
| macOS 12 (Monterey) | Office 2019/LTSC 2021 v16.89.2 |
| macOS 11 (Big Sur) | Office 2019/LTSC 2021 v16.77 |
| macOS 10.15 (Catalina) | Office 2019/LTSC 2021 v16.66 |
| macOS 10.14 (Mojave) | Office 2019 v16.54 |
| macOS 10.13 (High Sierra) | Office 2019 v16.43 |
| macOS 10.10 (Yosemite) | Office 2016 v16.16.27 |
| macOS 10.6 (Snow Leopard) | Office 2011 v14.7.7 |

---

## Step 1 — Download the Office Suite Installer

| macOS | Version (Build) | Download |
| --- | --- | --- |
| macOS 14+ (Sonoma) | 16.107.1 (26031524) | [Download](https://go.microsoft.com/fwlink/?linkid=525133) |
| macOS 13 (Ventura) | 16.101 (25091314) | [Download](https://officecdn.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_365_and_Office_16.101.25091314_Installer.pkg) |
| macOS 12 (Monterey) | 16.89.2 (24091630) | [Download](https://officecdn.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_365_and_Office_16.89.24091630_Installer.pkg) |
| macOS 12 (Monterey) alternate | 16.78.3 (23102801) | [Download](https://officecdn.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_365_and_Office_16.78.23102801_Installer.pkg) |
| macOS 11 (Big Sur) | 16.77 (23091003) | [Download](https://officecdn.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_365_and_Office_16.77.23091003_Installer.pkg) |
| macOS 10.15 (Catalina) | 16.66 (22100900) | [Download](https://officecdnmac.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_Office_16.66.22101101_Installer.pkg) |
| macOS 10.14 (Mojave) | 16.54 (21101001) | [Download](https://officecdn.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_Office_16.54.21101001_Installer.pkg) |
| macOS 10.13 (High Sierra) | 16.43 (20110804) | [Download](https://officecdn.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_Office_16.43.20110804_Installer.pkg) |
| macOS 10.10 (Yosemite) | 16.16.27 | [Download](https://officecdn.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_Office_16.16.20101200_Installer.pkg) |
| macOS 10.6 (Snow Leopard) | 14.7.7 | [Download](https://officecdn-microsoft-com.akamaized.net/PR/MacOffice2011/en-us/MicrosoftOffice2011.dmg) |

---

## Step 2 — Download the VL Serializer

The VL Serializer activates Office locally and permanently — no server contact needed after install.

| Serializer | Office Version | macOS Requirement | Download |
| --- | --- | --- | --- |
| Office 2024 LTSC VL Serializer | Office 2024 LTSC | macOS 13 (Ventura) and above | [Download](https://github.com/alsyundawy/Microsoft-Office-For-MacOS/blob/master/DATA/Microsoft_Office_LTSC_2024_VL_Serializer.pkg) |
| Office 2021 LTSC VL Serializer | Office 2021 LTSC | macOS 12 (Monterey) and above | [Download](https://github.com/alsyundawy/Microsoft-Office-For-MacOS/raw/master/DATA/Microsoft_Office_LTSC_2021_VL_Serializer.pkg) |
| Office 2021 LTSC VL Serializer MSDN ISO | Office 2021 LTSC | macOS 12 (Monterey) and above | [Download](https://github.com/alsyundawy/Microsoft-Office-For-MacOS/raw/master/DATA/SW_DVD5_Office_Mac_Serializer_2021_MLF_X22-74226.ISO) |
| Office 2019 VL Serializer | Office 2019 | Up to build 16.78 | [Download](https://github.com/alsyundawy/Microsoft-Office-For-MacOS/raw/master/DATA/Microsoft_Office_2019_VL_Serializer_Universal.pkg) |
| Office 2019 VL Serializer (Max 16.68) | Office 2019 | macOS Big Sur or earlier | [Download](https://github.com/alsyundawy/Microsoft-Office-For-MacOS/raw/master/DATA/Microsoft_Office_2019_VL_Serializer.pkg) |
| Office 2016 VL Serializer v2 | Office 2016 | — | [Download](https://github.com/alsyundawy/Microsoft-Office-For-MacOS/raw/master/DATA/Microsoft_Office_2016_VL_Serializer_2.0.pkg) |
| Office 2011 VL Serializer | Office 2011 | — | [Download](https://github.com/alsyundawy/Microsoft-Office-For-MacOS/raw/master/DATA/vlmsommxi.dmg) |

---

## Step 3 — Install Office

Double-click the downloaded `.pkg` file and follow the prompts.

Or via Terminal:

```bash
sudo installer -pkg ~/Downloads/Microsoft_365_and_Office_*.pkg -target /
```

> Wait for the installation to complete. This may take several minutes.

---

## Step 4 — Apply the VL Serializer

Double-click the serializer `.pkg` and follow the prompts.

Or via Terminal:

```bash
sudo installer -pkg ~/Downloads/Microsoft_Office_LTSC_2024_VL_Serializer.pkg -target /
```

---

## Step 5 — Disable Cloud Login Prompts

Run these commands in Terminal to suppress sign-in prompts:

```bash
defaults write com.microsoft.Word UseOnlineContent -integer 0
defaults write com.microsoft.Excel UseOnlineContent -integer 0
defaults write com.microsoft.Powerpoint UseOnlineContent -integer 0
```

---

## Step 6 — Open Any Office App

Open **Word**, **Excel**, or any Office app — it should launch directly without any sign-in prompt.

> If it still asks you to sign in, see the **Troubleshooting** section below.

---

## Step 7 — Optional: Disable Telemetry

```bash
defaults write com.microsoft.Word SendAllTelemetryEnabled -bool FALSE
defaults write com.microsoft.Excel SendAllTelemetryEnabled -bool FALSE
defaults write com.microsoft.Powerpoint SendAllTelemetryEnabled -bool FALSE
defaults write com.microsoft.Outlook SendAllTelemetryEnabled -bool FALSE
defaults write com.microsoft.onenote.mac SendAllTelemetryEnabled -bool FALSE
defaults write com.microsoft.autoupdate2 SendAllTelemetryEnabled -bool FALSE
defaults write com.microsoft.Office365ServiceV2 SendAllTelemetryEnabled -bool FALSE
```

---

## KMS Activation (Windows Only)

> On Mac, Office does not support KMS activation via command line. Use the VL Serializer instead.
> The KMS server below is for **Windows machines only**.

**KMS Server:** `kms.danipras.dev:1688`

### Verify KMS Connectivity

```bash
nc -zv kms.danipras.dev 1688
```

Expected output: `Connection to kms.danipras.dev 1688 port [tcp/*] succeeded!`

### Configure KMS on Windows

Run in an elevated Command Prompt on the Windows machine:

```cmd
cscript "C:\Program Files\Microsoft Office\Office16\ospp.vbs" /sethst:kms.danipras.dev
cscript "C:\Program Files\Microsoft Office\Office16\ospp.vbs" /setprt:1688
cscript "C:\Program Files\Microsoft Office\Office16\ospp.vbs" /act
```

> KMS activation renews every **7 days** — the server must remain reachable.

---

## Troubleshooting

### "Sign in to activate" prompt still appears after VL Serializer install

This is almost always caused by **cached Microsoft account credentials in Keychain**.

#### Step 1 — Sign out inside each Office app

Open Word → click the account icon (top right) → **Sign Out**. Repeat for Excel, PowerPoint, Outlook.

#### Step 2 — Remove cached credentials from Keychain

```bash
security delete-generic-password -s "Microsoft Office" 2>/dev/null
security delete-internet-password -s "login.microsoftonline.com" 2>/dev/null
security delete-internet-password -s "login.microsoft.com" 2>/dev/null
```

Or manually: open **Keychain Access** app → search `Microsoft` → delete all entries.

#### Step 3 — Remove Group Containers

```bash
sudo pkill -f "Microsoft"
sudo rm -rf ~/Library/Group\ Containers/UBF8T346G9.Office
sudo rm -rf ~/Library/Group\ Containers/UBF8T346G9.ms
```

#### Step 4 — Reboot, then re-apply Step 4 and Step 5 above

---

### Full Clean Reset (if nothing else works)

Use this when you need a completely fresh start — e.g., after accidentally installing the wrong serializer or a previous activation conflict.

```bash
# 1. Quit all Office apps
sudo pkill -f "Microsoft"

# 2. Run the License Removal Tool (download first)
# https://go.microsoft.com/fwlink/?linkid=849815
sudo installer -pkg ~/Downloads/Microsoft_Office_License_Removal_2.7.pkg -target /
```

Then **reboot your Mac**, and:

```bash
# 3. Remove Group Containers (residual license data)
sudo rm -rf ~/Library/Group\ Containers/UBF8T346G9.Office
sudo rm -rf ~/Library/Group\ Containers/UBF8T346G9.ms
sudo rm -rf ~/Library/Group\ Containers/UBF8T346G9.OneDriveStandaloneSuite

# 4. Remove cached credentials
security delete-generic-password -s "Microsoft Office" 2>/dev/null
security delete-internet-password -s "login.microsoftonline.com" 2>/dev/null
security delete-internet-password -s "login.microsoft.com" 2>/dev/null
```

Then repeat from **Step 3** (Install Office) above.

---

### Quick Reference — Common Errors

| Problem | Cause | Fix |
| --- | --- | --- |
| "Sign in to activate" after VL Serializer | Cached Microsoft account in Keychain | Clean Keychain + remove Group Containers, then reapply serializer |
| Office apps won't open after install | Incomplete installation | Re-run suite installer from Step 1 |
| Serializer installed but Office still in trial mode | Old license files conflicting | Run License Removal Tool, reboot, reapply serializer |
| `nc` to KMS port fails — "Network is unreachable" | Not on the right network / VPN not connected | Connect to VPN or correct network first |
| `nc` to KMS port fails — "Connection refused" | KMS server down or wrong port | Verify port — standard KMS is `1688`, not `1866` |
| Sign-in prompt returns after reboot | `UseOnlineContent` not set | Re-run Step 5 commands |

---

## Tools & Resources

| Tool | Link |
| --- | --- |
| License Removal Tool 2.7 | [Download](https://go.microsoft.com/fwlink/?linkid=849815) |
| Microsoft AutoUpdate | [Download](https://go.microsoft.com/fwlink/?linkid=830196) |
| Office-Reset Tool | [office-reset.com](https://office-reset.com/) |
| Office for Mac update history | [learn.microsoft.com](https://learn.microsoft.com/en-us/officeupdates/update-history-office-for-mac) |
| alsyundawy/Microsoft-Office-For-MacOS | [GitHub](https://github.com/alsyundawy/Microsoft-Office-For-MacOS) |

---

*Based on [alsyundawy/Microsoft-Office-For-MacOS](https://github.com/alsyundawy/Microsoft-Office-For-MacOS). Last updated: 2026-03-25.*
