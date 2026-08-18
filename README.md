# 🟣 YORVOXX — InstaHelp Console

> **YORVOXX InstaHelp — Android / Termux Account Support Console**

A Bash-based interactive console for Termux on Android with a terminal UI, account-support workflow, server-side license authentication, backend monitoring, device information, and Telegram support shortcuts.

## ✨ Features

- Professional terminal interface
- YORVOXX ASCII branding
- Instagram console
- Android / Termux device detection
- Server-side license verification
- HWID generation
- Backend API communication
- Backend event reporting
- Username-based workflow
- API health monitoring
- Boot and script restart
- Telegram support shortcuts
- Automatic dependency checking

## 📋 Requirements

- Android device
- Termux
- Internet connection
- `curl`
- `sha256sum`
- Termux:API for the location functionality

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/sisirey12-rgb/INSTAHELP-BY-YORVOXX.git
cd INSTAHELP-BY-YORVOXX
chmod +x b.sh
./b.sh

Make the script executable:

```bash
chmod +x b.sh
```

Run it:

```bash
./b.sh
```

Or:

```bash
bash b.sh
```

## 🧭 Main Menu

```text
[01] Account Disabled
[02] Account Suspended
[03] Account Ban
[04] About YORVOXX
[05] Telegram / Support
[06] Boot Script
[07] Rerun Script
[08] Server Status
[00] Exit
```

## 🔐 License Authentication

The client communicates with the configured license API and submits the license information together with the generated HWID.

The server can determine:

- License status
- HWID binding
- Device limit
- Devices used
- Failure reason

Sensitive license logic and secrets should remain on the backend.

## 🌐 Server Architecture

```text
User
  ↓
b.sh
  ↓ HTTPS
YORVOXX Backend
  ├── License verification
  ├── Protected logic
  ├── Database
  └── Server secrets
```

The public Bash client should not contain private API keys, database passwords, signing keys, or other server secrets.

## 🔗 API Configuration

The client is configured to communicate with:

```text
License API:
https://voxxxxxx.onrender.com/api/activate

Backend:
https://scxxxxtsh.onrender.com

Event API:
https://scxxxxxtsh.onrender.com/api/script-event/event
```

Update these values in the configuration section of `b.sh` when using different infrastructure.

## 📊 Server Status

Use:

```text
08
```

to open the API status monitor.

The console checks:

```text
LICENSE SERVER
VOXX SERVER
EVENT API
```

and displays their availability.

## 📲 Telegram / Support

The console includes shortcuts for the configured Telegram destinations:

```text
Telegram User:
@yor_forg3r

Telegram Channel:
@yorxvox
```

These values can be changed in `b.sh`.

## 🛠️ Troubleshooting

### Permission denied

```bash
chmod +x b.sh
./b.sh
```

### curl missing

```bash
pkg install curl
```

### sha256sum missing

```bash
pkg install coreutils
```

### termux-pkg missing

Install Termux:API support:

```bash
pkg install termux-api
```

Then grant the required Android permissions.

### License API returns 403

Check:

1. License key
2. License API URL
3. Backend configuration
4. HWID/device binding
5. Server logs
6. API authentication requirements

## 🔄 Updating

```bash
cd YOUR_REPOSITORY
git pull
chmod +x b.sh
./b.sh
```

## 🔒 Security

Recommended architecture:

```text
PUBLIC
b.sh
  ↓
HTTPS
  ↓
PRIVATE BACKEND
  ↓
Protected logic + secrets
```

## 🧪 Testing Checklist

Before distribution:

```text
[ ] Script starts correctly
[ ] Server UI renders correctly
[ ] Main menu works
[ ] Username validation works
[ ] License input implementation
[ ] Event API responds
[ ] Workflow improved
[ ] Telegram links for support
[ ] Server status works
[ ] Rerun works
[ ] Exit works
```

## 👤 Developer

**YORVOXX**

Version: **4.1**

Platform: **TERMUX / ANDROID**

Project: **YORVOXX INSTAHELP**

## ⚠️ Disclaimer

This project is intended for legitimate account-support and missuse this.

Users are responsible for complying with the terms, policies, permissions, and applicable laws governing any platform or service they interact with.

The developer is not responsible for misuse, unauthorized access, or policy violations resulting from use of the software.
