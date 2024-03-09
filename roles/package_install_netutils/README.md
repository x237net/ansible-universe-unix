<!-- roles/package_install_netutils/README.md
  -- ========================================
  --
  -- Copying
  -- -------
  --
  -- Copyright (c) 2023 universe.unix authors and contributors.
  --
  -- This file is part of the *universe.unix* project.
  --
  -- *universe.unix* is a free software project. You can redistribute it and/or
  -- modify it following the terms of the MIT License.
  --
  -- This software project is distributed *as is*, WITHOUT WARRANTY OF ANY KIND;
  -- including but not limited to the WARRANTIES OF MERCHANTABILITY, FITNESS FOR
  -- A PARTICULAR PURPOSE and NONINFRINGEMENT.
  --
  -- You should have received a copy of the MIT License along with
  -- *universe.unix*. If not, see <http://opensource.org/licenses/MIT>.
  -->

universe.unix.package_install_netutils
======================================

Purpose
-------

The `universe.unix.package_install_netutils` role installs a set of network
related utilities.

Dependencies
------------

- `universe.unix.package_install`, to install the system packages.

Packages
--------

The below listed packages are installed by this role.

### Red Hat

- `bind-utils` – A collection of utilities for querying DNS (Domain Name System)
  name servers.
- `curl` – A command line tool for transferring data with URL syntax.
- `ethtool` – An utility to query and change settings such as speed, port,
  auto-negotiation, PCI locations and checksum offload on many network devices,
  especially of Ethernet devices.
- `ipcalc` – Provides a simple way to calculate IP information for a host or
  network.
- `iproute` – Contains networking utilities (`ip` and `rtmon`, for example)
  which are designed to use the advanced networking capabilities of the Linux
  kernel.
- `iputils` – Contains basic utilities for monitoring a network, including
  `ping`.
- `whois` – Searches for an object in a RFC 3912 database.
- `mtr` – Combines the functionality of the `traceroute` and `ping` programs in
  a single network diagnostic tool.
- `nmap-ncat` – A feature packed networking utility which will read and write
  data across a network from the command line.
- `openssh` – SSH (Secure SHell) is a program for logging into and executing
  commands on a remote machine.
- `rsync` – Uses a reliable algorithm to bring remote and host files into sync
  very quickly.
- `tcpdump` – A command-line tool for monitoring network traffic.
- `traceroute` – Displays the route used by IP packets on their way to a
  specified network (or Internet) host.
