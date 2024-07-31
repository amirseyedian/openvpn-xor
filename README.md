# openvpn-xor
 Openvpn patched with xor patch provided by tunnelbrick, compatible with debian based linux distrobutions and freebsd (OPNsense/PfSense)

### OpenVPN Custom Build

This repository contains instructions and patches for building a custom version of OpenVPN 2.6.11 with XOR scrambling options.
this is not the officially maintained openvpn package!


## Debian-based Distro

### Install Dependencies


`sudo apt install build-essential libssl-dev iproute2 liblz4-dev liblzo2-dev libpam0g-dev libpkcs11-helper1-dev libsystemd-dev resolvconf pkg-config autoconf automake libtool libcap-ng-dev libnl-genl-3-dev -y `

### Configure installer

`sudo ./configure --enable-systemd --enable-async-push --enable-iproute2 --enable-management --enable-plugins`

### Build

`make`

### Install

`sudo make install`

## FreeBSD-based (PfSense/OPNsense)

**First enable Freebsd repository**

### Install dependencies 

`pkg install lang/gcc pkgconf autoconf libtool automake autoconf`


### Configure installer

`./configure --enable-async-push --enable-management --enable-plugins`

### Build

`make`

### Install

`make install`

