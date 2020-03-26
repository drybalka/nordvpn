Nordvpn
=======

Introduction
------------

This is a radical simplification of a great script by nstinus
that now uses nordvpn api to find the recommended server.

`nordvpn` is a command line helper script to use nordvpn.com for
systems with `openvpn` and `systemd`.
It was created for Arch Linux but should run without too much
difficulty on systems that satisfy the following dependency list:
- openvpn,
- systemd,
- curl,
- unzip,
- jq,
- have vpnfailsafe.sh script in /etc/openvpn

You may also want to consider disabling ipv6 during connection by editing
corresponding lines in "disable/enable_ipv6()" in order to protect against
ipv6 leaking.

Quickstart
----------

- Once installed, run `sudo nordvpn update` to download and install the
configuration files.
- Edit `/etc/openvpn/client/nordvpn/credentials.conf`.
- Run `sudo nordvpn connect` to connect to a recommended nordvpn server.
- Run `sudo nordvpn connect server_name` to connect to this server 
(i.e. "us1234"). Only UDP connections are available.
- Run `sudo nordvpn connect country_name` to connect to a recommended
server in this country (i.e. "us", "germany", etc.).
- The status command shows you the status of the systemd service.
- Run `sudo nordvpn disconnect` to end the connection.
- See `sudo nordvpn -h` for more information.
