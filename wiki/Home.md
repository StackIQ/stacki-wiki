## Getting Started

Stacki is an extremely fast and scalable data center bare metal installer and is part of the Teradata family of open source projects - developed and supported by the Shared Services team at Teradata (formerly the wacky bunch of engineers from StackIQ).

So yeah, there's that.

On Stacki 5.x we currently DO NOT support installing CentOS/RHEL 6.x systems.

If any of the terms below are unfamiliar to you, read the [Definitions](Definitions).

## Installation

You need one frontend and at least one backend.  They need to be networked.  The backend needs to be set to PXE boot.

You can't install a backend without a frontend.

You can't install a frontend without an OS pallet AND the stacki pallet.

Which means the [stackios](https://github.com/Teradata/stacki/releases/download/stacki-5.4.1/stackios-5.4.1-redhat7.x86_64.disk1.iso) pallet may be ideal for you. Please note that Stacki 5.4.1 is the last release that shipped stackios.  The way to install 5.6 is on top of an existing CentOS/RHEL/SLES system.

If you're an experiential learner and don't need/want explanations follow the [Quickstart](Quickstart).

If you have already installed a CentOS/RHEL/some variant and don't want to rebuild that server, follow: [Frontend Install - Existing System](Frontend-Install-Existing).

If you don't have an installed frontend and need painfully detailed instructions, potentially HR-violating side commentary, and general ranting and railing, start with the full stackios iso and use: [Frontend Install - New](Frontend-Install-New).

If you don't actually have an internal or external DVD, use  [Frontend Installation From USB](Frontend-Installation-From-USB).

Then install backends. Either continue using the [Quickstart](Quickstart) or:

* If you control your installing network and you're lazy, follow: [Backend Install - Discovery](Backend-Install-Discovery)
* If you have enterprise-y needs, i.e. you have neurotic, paranoid, and/or obstreperous security or network teams who require you to map hostname/ip/mac address to limit the DHCP queries to a specific subnet, use: [Backend Install -  Spreadsheet](Backend-Install-Spreadsheet)

### Customization

If you give a mouse a cluster.....

Once you've done all that and have a default frontend and a default backend up, you'll want to start [Customization](Customization).

The general work flow is:

* Create a Cart
* Add packages and kickstart config (partitions, controllers, scripts)
* Reinstall backend(s)
* Check/test.
* Fix or do more configuration.
* Rinse, repeat. Stop when happy.

### Downloads
Get them all right here:

**This pallet is the StackiOS 5.4.1 ISO**

[stackios-5.4.1-redhat7.x86_64.disk1.iso](https://github.com/Teradata/stacki/releases/download/stacki-5.4.1/stackios-5.4.1-redhat7.x86_64.disk1.iso) (MD5: 03daf2291e8d6617f8ae1f4d5e821ed6)

**Individual Pallets**

For building on an already installed server.

With Stacki 5.6.5:

[stacki-5.6.5-redhat7.x86_64.disk1.iso](https://github.com/Teradata/stacki/releases/download/stacki-5.6.5/stacki-5.6.5-redhat7.x86_64.disk1.iso) (MD5: de43aea1da528cc954388d03ecb5f978)

With Stacki 5.4.1:

[stacki-5.4.1-redhat7.x86_64.disk1.iso](https://github.com/Teradata/stacki/releases/download/stacki-5.4.1/stacki-5.4.1-redhat7.x86_64.disk1.iso) (MD5: 9e1c159ec4a34396b0d4c9c88d6c0b95)

For either version of stacki, you will also need a [CentOS 7.6](http://archive.kernel.org/centos-vault/7.6.1810/isos/x86_64/) iso. I use the Everything version but you can use smaller DVD one (which has less packages). You can also use a RHEL 7.6 iso if you want to run Redhat Enterprise.  SLES12 and 15 will also work as a stacki Frontend, but you must build the stacki SLSE pallet yourself.

If you're installing stacki on a pre-installed CentOS/RHEL/SLES machine you'll need the **frontend-install.py** script as well.  On stacki 5.4.1 and later, this is part of the frontend install process and the script is included in the ISO itself.  Mount the iso then find and install the stacki-fab*rpm and foundation-python-3*rpm.
