---
layout: doc
title: qvm-firewall
permalink: /doc/tools/3.2/dom0/qvm-firewall/
redirect_from:
- /doc/dom0-tools/qvm-firewall/
- /en/doc/dom0-tools/qvm-firewall/
- /doc/Dom0Tools/QvmFirewall/
- /wiki/Dom0Tools/QvmFirewall/
---

```
============
qvm-firewall
============

NAME
====
qvm-firewall - manage VM's firewall rules

SYNOPSIS
========
| qvm-firewall [-n] <vm-name> [action] [rule spec]

Rule specification can be one of:
    1. address|hostname[/netmask] tcp|udp port[-port]
    2. address|hostname[/netmask] tcp|udp service_name
    3. address|hostname[/netmask] any

OPTIONS
=======
-h, --help
    Show this help message and exit
-l, --list
    List firewall settings (default action)
-a, --add
    Add rule
-d, --del
    Remove rule (given by number or by rule spec)
-P SET_POLICY, --policy=SET_POLICY
    Set firewall policy (allow/deny)
-i SET_ICMP, --icmp=SET_ICMP
    Set ICMP access (allow/deny)
-D SET_DNS, --dns=SET_DNS
    Set DNS access (allow/deny)
-Y SET_YUM_PROXY, --yum-proxy=SET_YUM_PROXY
    Set access to Qubes yum proxy (allow/deny).
    *Note:* if set to "deny", access will be rejected even if policy set to "allow"
-r, --reload
    Reload firewall (implied by any change action)
-n, --numeric
    Display port numbers instead of services (makes sense only with --list)
--force-root
    Force to run, even with root privileges

AUTHORS
=======
| Joanna Rutkowska <joanna at invisiblethingslab dot com>
| Rafal Wojtczuk <rafal at invisiblethingslab dot com>
| Marek Marczykowski <marmarek at invisiblethingslab dot com>
```

-----

**Note:** The Markdown source of this page in [`qubes-doc`] was generated by
running the [`update-manpages`] script on `qubes-core-admin/doc/qvm-tools/`.
If you wish to update the contents of this page as it appears on the Qubes OS
website, please submit a pull request to change the appropriate file in
`qubes-core-admin/doc/qvm-tools/`. Do not attempt to change the Markdown source
of this page in [`qubes-doc`] directly. All direct changes to the Markdown file will be
overwritten the next time this page is regenerated.

[`qubes-doc`]: https://github.com/QubesOS/qubes-doc/
[`update-manpages`]: https://github.com/QubesOS/qubesos.github.io/blob/master/_utils/update-manpages
