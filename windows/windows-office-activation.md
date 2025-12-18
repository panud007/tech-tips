# Windows and Office Activation Guide

## Overview

This guide provides a free activation solution for Windows and Microsoft Office using the Microsoft Activation Scripts (MAS) tool.

## What is MAS (Microsoft Activation Scripts)?

MAS is an open-source collection of scripts for activating Microsoft products using:

- **HWID** - Digital License activation for Windows 10/11
- **Ohook** - Permanent activation for Office
- **KMS38** - Activation until 2038 for Windows 10/11
- **Online KMS** - 180-day activation for Windows/Office

The tool is hosted at [get.activated.win](https://get.activated.win) and maintained by the community.

## Prerequisites

- Windows 10 or Windows 11
- Administrator privileges
- Internet connection
- Microsoft Office installed (if activating Office)

## Usage Instructions

### Method 1: Using the Batch Script (Recommended)

1. **Locate the script**
   - Navigate to: `tech-tips/windows/Activator_WinOffice.bat`

2. **Run as Administrator**
   - Right-click on `Activator_WinOffice.bat`
   - Select **"Run as administrator"**
   - Click **"Yes"** when prompted by UAC

3. **Follow the activation wizard**
   - A PowerShell window will open with the activation menu
   - Choose your activation method:
     - `[1] HWID` - For Windows (permanent)
     - `[2] Ohook` - For Office (permanent)
     - `[3] KMS38` - For Windows (until 2038)
     - `[4] Online KMS` - For Windows/Office (180 days)

4. **Wait for completion**
   - The script will automatically activate your product
   - You'll see a success message when done

### Method 2: Manual PowerShell Command

If you prefer to run the command directly:

```powershell
irm https://get.activated.win | iex
```

**Steps:**

1. Open PowerShell as Administrator
2. Paste the command above
3. Press Enter
4. Follow the on-screen menu

## Activation Methods Explained

### HWID (Hardware ID)

- **Best for:** Windows 10/11
- **Duration:** Permanent
- **Type:** Digital License
- **Pros:** Survives reinstalls, tied to hardware
- **Cons:** Only works for Windows

### Ohook

- **Best for:** Office 2016/2019/2021/365
- **Duration:** Permanent
- **Type:** License hook
- **Pros:** Permanent activation, no expiration
- **Cons:** Office only

### KMS38

- **Best for:** Windows 10/11 Enterprise/Education
- **Duration:** Until 2038
- **Type:** KMS activation
- **Pros:** Long-term activation
- **Cons:** Requires specific Windows editions

### Online KMS

- **Best for:** Quick temporary activation
- **Duration:** 180 days (auto-renewal)
- **Type:** KMS activation
- **Pros:** Works for both Windows and Office
- **Cons:** Requires periodic renewal

## Troubleshooting

### Script doesn't run

- **Solution:** Make sure you're running as Administrator
- Right-click → "Run as administrator"

### PowerShell execution policy error

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

### Antivirus blocking the script

- **Reason:** Some antivirus software may flag activation scripts
- **Solution:** Temporarily disable antivirus or add exception
- **Note:** The MAS tool is open-source and safe

### Activation failed

1. Check your internet connection
2. Ensure Windows/Office is genuine (not pirated copy)
3. Try a different activation method
4. Check Windows Update is not pending

### "Product key not found" error

- Some Windows editions may not support certain activation methods
- Try HWID method for Windows 10/11 Home/Pro
- Try KMS38 for Enterprise/Education editions

## Checking Activation Status

### For Windows

1. Press `Win + R`
2. Type: `slmgr /xpr`
3. Press Enter

Or check in Settings:

- Settings → System → Activation

### For Office

1. Open any Office app (Word, Excel, etc.)
2. Go to File → Account
3. Check "Product Information" section

## Legal Considerations

> [!IMPORTANT]  
> **Educational Purpose**: This guide is provided for educational and testing purposes.

> [!WARNING]  
> **License Compliance**: While these activation methods use legitimate Microsoft technologies, using them without a valid license may violate Microsoft's Terms of Service. Always ensure you have proper licensing for production environments.

> [!NOTE]  
> **Recommended**: For businesses and production use, purchase genuine licenses from Microsoft or authorized resellers.

## Alternative Activation Methods

1. **Purchase Genuine License**
   - Microsoft Store
   - Authorized resellers
   - Volume licensing (for businesses)

2. **Free Legitimate Options**
   - Windows 10/11: Use without activation (limited personalization)
   - Office: Use Office Online (free web version)
   - Office: Microsoft 365 trial (1 month free)

## Additional Resources

- **MAS GitHub Repository**: [https://github.com/massgravel/Microsoft-Activation-Scripts](https://github.com/massgravel/Microsoft-Activation-Scripts)
- **Official Website**: [https://massgrave.dev](https://massgrave.dev)
- **Documentation**: [https://massgrave.dev/docs](https://massgrave.dev/docs)

## Related Guides

- [Windows Performance Optimization](./optimize-windows.md)
- [Windows Update Troubleshooting](./fix-windows-update.md)

---

**Last Updated:** December 2025  
**Tested On:** Windows 10/11, Office 2016/2019/2021
