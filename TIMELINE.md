# Investigation Timeline

## Mar 13, 2025

### 09:44 AM
- Phishing email delivered from `update@windows-update.site`
- Recipient: `dylan@letsdefend.io`
- Subject: `Upgrade your system to Windows 11 Pro for FREE`

### 09:44 AM
- SIEM alert triggered:
  - `SOC338 - Lumma Stealer - DLL Side-Loading via Click Fix Phishing`

### 11:26 PM
- Internal host connected to `132.232.40.201` over HTTPS (TCP/443)

### 11:26:08 PM
- `chrome.exe` observed running under parent `explorer.exe`
- PID observed: `5188`

### 11:26:08 PM
- Chrome utility process behavior observed:
  - `unzip.mojom.Unzipper`
  - `quarantine.mojom.Quarantine`

## Assessment

The timeline supports the following chain:

1. phishing email delivery
2. delayed user interaction
3. connection to attacker-controlled infrastructure
4. suspicious archive processing in browser
5. no confirmed payload execution
