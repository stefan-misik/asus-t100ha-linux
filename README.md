# ASUS T100HA Bluetooth on Linux

As of writing of this document (July 2023) all hardware works out-of-the box,
except the following:

## Kernel Freezes

Put the following option on the kernel's command line to prevent random freezes:
```
intel_idle.max_cstate=1
```

## Bluetooth Doesn't Work

Download Bluetooth driver for Windows from
[ASUS Support](https://www.asus.com/supportonly/t100ha/helpdesk_download/),
install it inside Windows virtual Machine, and search for
`BCM43341B0_002.001.014.0122.0176.hcd` file within Windows installation folder.
Copy it to your Linux machine and place it in
`/lib/firmware/brcm/BCM43341B0.hcd`.
