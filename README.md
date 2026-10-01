# OverRoute v2

**OverRoute** is a network-level MDM bypass designed for managed iPads.

v2 is the updated version of OverRoute, rebuilt to work with the newer **Jamf-based MDM environment**.
It does not remove the MDM profile or jailbreak the device. Instead, it interferes with the network communication used by the management system, allowing the device to operate without actively receiving new management instructions.

---

# READ FIRST!

Before using OverRoute, understand what you're doing.

* This totally will interfere with device management.
* You can get caught if you're using it on a device managed by someone else.
* You are responsible for how you use it.

**Use OverRoute only on devices you own or where you have permission to test it.**

---

## What is OverRoute?

OverRoute started as a simple experiment for bypassing the older Avrio/eSchoolPad MDM setup, then the MDM provider changed to Jamf.

**OverRoute v2 is the response to that**

Instead of targeting the old MDM infrastructure, v2 is built around the newer **Jamf-managed environment**.

The basic idea remains simple and is still the same:
**If the device can't communicate with the management server, the management server can't immediately push new instructions to it.**
The MDM profile itself is still installed, but can't work.

---

## What v2 does

OverRoute v2 is designed to interfere with the network communication between the iPad and its MDM infrastructure.

This can prevent things such as:

* MDM check-ins
* Remote configuration changes
* New restriction pushes
* Management commands
* Other management traffic that depends on the MDM connection

---

## v1 vs v2

### OverRoute v1

The original version targeted the old Avrio MDM infrastructure.
It was built around blocking the known MDM endpoint and preventing the device from checking in.
It worked surprisingly well for what started as an experiment.

Then the school changed the MDM.

### OverRoute v2

v2 is the updated implementation for the **Jamf-based deployment**.

The goal isn't to remove supervision or modify the iPad itself.

Instead, v2 adapts the original network-level approach to the new management system.

**v1 → Avrio/eSchoolPad**

**v2 → Jamf**

---

## What OverRoute does NOT do

OverRoute does not:

* Remove the MDM profile
* Remove supervision
* Jailbreak the iPad
* Modify iOS system files
* Permanently unenroll the device
* Magically make the device unmanaged

The device is still managed.

OverRoute works by disrupting the communication that management depends on.

If normal communication with the MDM infrastructure is restored, management can return.

---

## Why I made this

OverRoute wasn't originally some giant security project.
I made it because I was tired of dealing with an MDM that constantly got in the way.
The first version was basically "What happens if I stop the MDM from calling home?"
That turned into OverRoute v1.
Then the school moved to Jamf.
So naturally, instead of accepting defeat like a normal person, I rebuilt it.
That became **OverRoute v2**.

---

## Status

**OverRoute v2 — Working**

v2 is the current version made for the newer Jamf-based environment.
The implementation may need to change again if the MDM infrastructure changes.. hopefully not

---

## Disclaimer
**Don't be stupid**
**Use responsibly.**
