# OverRoute v1 🙌

**OverRoute** is a DNS-level firewall and route manipulator built to block MDM servers on demand — giving the user full control over a locked-down iPad environment.

---

# READ FIRST!

Before installation, i'd just like to inform you about the risks of this, etc.
- It is possible that you may get caught red handed. **YOU WILL BE RESPONSIBLE FOR THIS!!**
- This is a very powerful tool.
- Read everything. Im being serious.
- Stay vigilant.

---

## Purpose

This tool is designed to **disable MDM enforcement** by cutting off its connection to its command server, effectively freezing all restrictions and making the device act “normal” — but free.

OverRoute v1 uses DNS blocking and route spoofing to prevent:

- MDM check-ins
- MDM config pushes
- MDM profile removals from reporting

---

## Features

- Blocks MDM server (`sa.eschoolpad.net/server`)
- Prevents `/checkin/dlsu` beaconing
- No need to remove profile (keeps device "compliant")
- Fast toggle between ON/OFF (once only)
- Zero jailbreak or sideload needed
- Works even on supervised iPads

---

## How It Works

1. MDM tries to call home to `https://sa.eschoolpad.net/server/checkin/dlsu`
2. OverRoute v1 **BLOCKS** the domain entirely.
3. Device **cannot talk** to MDM, freezing it in place
4. Profile is never removed, so **no “check-out” alert is triggered**

---

## Usage

> This version assumes you're using an iPad (like the required device, dude.)

### 1. Install DNS

on iPad Safari:
```url
https://bit.ly/overroute
```

Install it → blocks MDM routing.

---

## Notes

- MDM will silently **fail to update or apply restrictions**
- If device goes online and connects to the real MDM server, it will **re-apply all policies**
- Profile is still installed, just inert
- This is a passive bypass — **no tampering of the profile or OS**

---

##  Coming in OverRoute v2

-  Toggle MDM on/off in Web UI
-  Fake MDM server with Flask
-  Auto-reinstall MDM profiles (signed)
-  Silent “anti-checkout” beacon blocker
-  Logging + Scheduler

---

## ⚠️ Disclaimer

This tool is for **educational purposes only**. It should not be used to bypass institutional security policies without permission.  
Use responsibly.
