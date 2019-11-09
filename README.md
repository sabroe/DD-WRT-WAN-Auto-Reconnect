# DD-WRT-WAN-Auto-Reconnect

DD-WRT startup script "wan-auto-reconnect.startup".

Monitors WAN connectivity, reconnects if necessary.
It is an intended goal to detect loss of internet access and reconnect
_without_ disturbing ongoing communication on the inner LAN network.

This was originally intended for a vehicular application connecting with a 3G
dongle, and it may apply for unstable ISPs messing around with their networks
and their customers.

To test, this may be run directly.
To force a loss of connectivity, try "stopservice wan".

To install, this may be stored as e.g.
/jffs/etc/config/wan-auto-reconnect.startup
To address any concerns about router script size restrictions, feel free to strip the comments during installation.
Test scope:
* DD-WRT v3.0-r33345 std (09/11/17), Linksys WRT1200ACSv2, basic dialup with 3G dongle (D-Link DWR 157 rev. B).
* DD-WRT v3.0-r33345 std (09/11/17), Linksys WRT1900ACSv2, basic setup as second router behind ISP specific, enforced first router with fiber connectivity.
* IPv4 only, for now.

**://Morten Sabroe Mortensen**
