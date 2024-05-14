![Logo](https://avatars.githubusercontent.com/u/151680118?s=200&v=4 "Logo")

**[↤ Getting Started](../README.md)**

Install Launch Agents
===

> All we have left to do now is install the Launch Agents to handle starting & stopping your sandbox.

Make sure you are in the root of this project, and run the installer:

```bash
./install
```

Security Overview
---

> Your IT Department might want to know a few things about what this tool is doing.

### Overview

**NOTE:** This tool does not require a superuser or root-level access to install.

Our [./install](../install) script does the following:

1. Uses [Homebrew](https://brew.sh) to install [sleepwatcher](https://formulae.brew.sh/formula/sleepwatcher) to add event listeners for Awake & Sleep states
2. Adds [sdx-start](../bin/sdx-start) bash script to start a Sandbox after the computer boots or wakes up
3. Adds [sdx-stop](../bin/sdx-stop) bash script to stop a Sandbox when the computer shuts down or goes to sleep
4. Adds [boot-shutdown](../bin/boot-shutdown) bash script to call above scripts on shutdown and boot
5. Adds [com.opensfcc.sleepwatcher.plist](../launchd/com.opensfcc.sleepwatcher.plist) Launch Agent for Sleepwatcher events
6. Adds [com.opensfcc.sandbox.plist](../launchd/com.opensfcc.sandbox.plist) Launch Agent for Boot and Shutdown events

### Installation Prompts

After running the installer, you will see a notice for a new `Background Items Added` entry for [boot-shutdown](../bin/boot-shutdown).  This was registered by the [com.opensfcc.sandbox.plist](../launchd/com.opensfcc.sandbox.plist) Launch Agent when we requested to be notified as the computer started or was about to shut down.

Clicking this notice will open the Login Items, where our [boot-shutdown](../bin/boot-shutdown) script is listed.

![background-items](./img/security-background-items.png "background-items")

Clicking this notice will open the Login Items, where you will see our [boot-shutdown](../bin/boot-shutdown) script listed.

![login-items](./img/security-login-items.png "login-items")

---

[![Previous Step](https://img.shields.io/badge/Previous-121212.svg?logo=github&style=for-the-badge)](./fetch-sandbox-uuid.md) &nbsp; [![Next Step](https://img.shields.io/badge/All_Done-1aa0db.svg?logo=github&style=for-the-badge)](../README.md)
