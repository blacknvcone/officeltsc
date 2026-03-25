# Office LTSC 2024 Installation & KMS Activation Guide

> **KMS Server:** `192.168.172.21:1688`

---

## Prerequisites

- Windows 10/11 or Windows Server 2019/2022
- Administrator privileges
- Internet access (for downloading Office files, ~3GB)
- KMS server reachable at `192.168.172.21:1688`

---

## Step 1 — Download the Office Deployment Tool

1. Go to: https://www.microsoft.com/en-us/download/details.aspx?id=49117
2. Download and run `officedeploymenttool_*.exe`
3. Extract contents to `C:\ODT`

---

## Step 2 — Create Configuration File

Save the file at `C:\ODT\configuration-OfficeLTSC2024-Standard-x64.xml` with the following content:

```xml
<!-- Office LTSC Standard 2024 configuration file
     Volume License (KMS activation) - 64-bit
     Channel: PerpetualVL2024
     KMS Server: 192.168.172.21:1688 -->

<Configuration ID="OfficeLTSC2024-Standard">

  <Add OfficeClientEdition="64" Channel="PerpetualVL2024">
    <Product ID="Standard2024Volume">
      <Language ID="en-us" />
      <ExcludeApp ID="Teams" />
      <ExcludeApp ID="OneDrive" />
      <ExcludeApp ID="Groove" />
      <ExcludeApp ID="Lync" />
    </Product>
  </Add>

  <Updates Enabled="TRUE" />

  <RemoveMSI />

  <Property Name="SharedComputerLicensing" Value="0" />
  <Property Name="FORCEAPPSHUTDOWN" Value="TRUE" />
  <Property Name="DeviceBasedLicensing" Value="0" />

  <Display Level="Full" AcceptEULA="TRUE" />

</Configuration>
```

> **Note:** Change `Language ID` to your locale (e.g., `id-id` for Indonesian, `en-us` for English).
> Add or remove `<ExcludeApp />` lines to customize which apps get installed.

---

## Step 3 — Download Office Files

Open **Command Prompt as Administrator** and run:

```cmd
cd C:\ODT
setup.exe /download configuration-OfficeLTSC2024-Standard-x64.xml
```

> This downloads approximately 3GB of Office installation files into `C:\ODT`.

---

## Step 4 — Install Office

Still in the same Administrator Command Prompt, run:

```cmd
setup.exe /configure configuration-OfficeLTSC2024-Standard-x64.xml
```

> Wait for the installation to complete. Do not close the window.

---

## Step 5 — Activate with KMS Server

Open a **new Command Prompt as Administrator**, then run the following commands one by one:

```cmd
cd "C:\Program Files\Microsoft Office\Office16"
```

### 5a — Enter the GVLK (Generic Volume License Key)

```cmd
cscript ospp.vbs /inpkey:V28N4-JG22K-W66P8-VTMGK-H6HGR
```

### 5b — Set KMS Server Address

```cmd
cscript ospp.vbs /sethst:192.168.172.21
```

### 5c — Set KMS Port

```cmd
cscript ospp.vbs /setprt:1688
```

### 5d — Trigger Activation

```cmd
cscript ospp.vbs /act
```

### 5e — Verify Activation Status

```cmd
cscript ospp.vbs /dstatus
```

> Look for `LICENSE STATUS: ---LICENSED---` to confirm successful activation.

---

## GVLK Keys Reference

| Product | GVLK Key |
|---|---|
| Office LTSC Professional Plus 2024 | `XJ2XN-FW8RK-P4HMP-DKDBV-GCVGB` |
| Office LTSC Standard 2024 | `V28N4-JG22K-W66P8-VTMGK-H6HGR` |
| Project Professional 2024 | `FQQ23-N4YCY-73HQ3-FM9WC-76HF4` |
| Project Standard 2024 | `PD3TT-NTHQQ-VC7CY-MFXK3-G87F8` |
| Visio LTSC Professional 2024 | `B7TN8-FJ8V3-7QYCP-HQPMV-YY89G` |
| Visio LTSC Standard 2024 | `JMMVY-XFNQC-KK4HK-9H7R3-WQQTV` |

---

## Troubleshooting

| Error Code | Meaning | Fix |
|---|---|---|
| `0xC004F074` | KMS server unreachable | Ensure firewall allows TCP port `1688` to `192.168.172.21` |
| `0xC004F038` | KMS client count too low | KMS requires minimum 5 Office activations in the pool |
| `0x8007007B` | Invalid product key format | Re-enter the GVLK key carefully |
| Office dir not found | Wrong installation path | Try `C:\Program Files (x86)\Microsoft Office\Office16` instead |

### Check KMS connectivity manually

```cmd
telnet 192.168.172.21 1688
```

> If the connection fails, contact your network/server admin to verify the KMS service is running.

---

## Notes

- Activation is valid for **180 days** and auto-renews every **7 days** when the KMS server is reachable.
- If the machine goes offline for extended periods, re-run `cscript ospp.vbs /act` to renew manually.
- To check remaining grace period: `cscript ospp.vbs /dstatus`

---

*Guide applies to Office LTSC 2024 (Volume License). Last updated: 2026-03-25.*
