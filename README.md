# OpenCore ESP Backup for HP 245 G9 (6Q8M2ES)

I've installed macOS Monterey onto my laptop finally but I wasn't able to fix some hardwares.

CPU: AMD Ryzen 5 5625U with its internal GPU

Drive: WD_BLACK SN770 2TB

Network: Realtek RTL8111 + Intel AX200

Audio: Realtek ALC236

# Here's the bugs

*internal microphone

*trackpad (I couldn't try VoodooI2C because macOS doesn't boot while DSDT active)

*hibernation (I tried HibernationFixup.kext, macOS doesn't boot)

*I've not tried audio jack and Ethernet right now.
