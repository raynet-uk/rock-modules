<div align="center">

![RAYNET UK](https://www.raynet-uk.net/technical/graphics/raynet-uk.gif)

# ROCK Module Repository
### Official modules for the ROCK platform — RAYNET Operational Control Kernel

[![RAYNET UK](https://img.shields.io/badge/RAYNET-UK%20Affiliated-C8102E?style=flat-square&labelColor=003366)](https://www.raynet-uk.net)
[![License](https://img.shields.io/badge/License-GPL--2.0-blue?style=flat-square)](https://www.gnu.org/licenses/gpl-2.0.html)
[![Platform](https://img.shields.io/badge/Platform-Laravel%2012-red?style=flat-square)](https://laravel.com)
[![PHP](https://img.shields.io/badge/PHP-8.2%2B-777BB4?style=flat-square)](https://php.net)
[![ROCK](https://img.shields.io/badge/Core-ROCK-003366?style=flat-square)](https://github.com/raynet-uk/rock)

</div>

---

## What is ROCK?

**ROCK** (RAYNET Operational Control Kernel) is a web platform built specifically for **RAYNET UK** group websites. It is developed and maintained by [RAYNET Liverpool](https://raynet-liverpool.net) and is intended for use by RAYNET groups affiliated with [raynet-uk.net](https://www.raynet-uk.net).

> ⚠️ This platform is specifically designed for RAYNET UK groups and is built on Laravel 12.

### Who is it for?

- ✅ RAYNET UK affiliated groups
- ✅ Groups registered at [raynet-uk.net](https://www.raynet-uk.net)
- ✅ Groups looking to replace a static or ageing website
- ✅ Groups wanting member management, event scheduling, and training tracking built in

### Who is it NOT for?

- ❌ Non-RAYNET organisations
- ❌ RACES, ARES, or other international emergency comms groups (though inspiration is welcome!)

---

## Available Modules

| Code | Name | Version | Purpose |
|------|------|---------|---------|
| **BEACON** | Announcements | 1.0.0 | Broadcast & Emergency Announcement Control & Notification |
| **VAULT** | Drive | 1.0.0 | Verified Archive & Unified Library Tool |
| **ECHO** | Net Log | 1.0.0 | Electronic Communications History & Operations |
| **DEBRIEF** | After Action Report | 1.0.0 | Debrief, Review, Intelligence & Evaluation for Future Operational Performance |

*More modules coming soon — COMPASS (members), SENTINEL (incidents), ATLAS (mapping), CASCADE (callouts), and more.*

---

## For ROCK Group Administrators

Your ROCK installation checks this repository automatically. To browse and install modules:

1. Log in to your admin panel
2. Go to **Admin → Module Manager**
3. Click **Browse Modules**
4. Click **Install** on any module

Updates are downloaded and applied with a single click — no FTP or server access required.

---

## Features of ROCK

- 📄 **Page Builder** — Visual page editor
- 👥 **Member Management** — registrations, roles, callsign verification
- 📅 **Event Management** — scheduling, RSVPs, operator assignments, briefings
- 🎓 **Training & LMS** — courses, quizzes, SCORM support, certificates
- 🔔 **Alert Status** — live RAYNET alert level display
- 📡 **Ops Map** — APRS, Meshtastic, weather and flood overlays
- 🔌 **Module System** — extend with modules, auto-updates from this repo
- 🔐 **SSO / OAuth** — single sign-on for connected tools

---

## Publishing a Module Update

*For RAYNET Liverpool maintainers only.*

1. Zip the updated module: `zip -r ModuleName-X.Y.Z.zip ModuleName/`
2. Create a GitHub Release tagged `module-name-X.Y.Z`
3. Upload the zip as a release asset
4. Edit `registry.json` — update `version`, `download_url`, `changelog`
5. Commit and push — all installed ROCK sites pick it up on next update check

### Module ZIP Structure

```
ModuleName/
├── module.json
├── Providers/
│   └── ModuleNameServiceProvider.php
├── Http/
│   └── Controllers/
├── Resources/
│   └── views/
└── Database/
    └── Migrations/
```

### module.json Required Fields

```json
{
    "name": "MODULE_CODE",
    "alias": "module-alias",
    "system_code": "CODE",
    "full_name": "Full expansion of the code",
    "version": "1.0.0",
    "description": "What this module does.",
    "author": "RAYNET Liverpool",
    "providers": ["Modules\\ModuleName\\Providers\\ModuleNameServiceProvider"]
}
```

---

## Links

| | |
|--|--|
| 🌐 **RAYNET UK** | [raynet-uk.net](https://www.raynet-uk.net) |
| 📻 **RAYNET Liverpool** | [raynet-liverpool.net](https://raynet-liverpool.net) |
| 🔧 **ROCK Platform** | [github.com/raynet-uk/rock](https://github.com/raynet-uk/rock) |
| 📧 **Support** | [github.com/raynet-uk/rock/issues](https://github.com/raynet-uk/rock/issues) |

---

<div align="center">

*Robust. Resilient. Radio.*

ROCK is developed by RAYNET Liverpool for the benefit of RAYNET UK groups.
RAYNET is the Radio Amateurs' Emergency Network, affiliated with the RSGB.

`73 de G4BDS & M7NDN 📻`

</div>
