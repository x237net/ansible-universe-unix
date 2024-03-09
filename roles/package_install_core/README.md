<!-- roles/package_install_core/README.md
  -- ====================================
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

universe.unix.package_install_core
==================================

Purpose
-------

The `universe.unix.package_install_core` role installs the bare minimum list of
packages required for a pleasant operating system experience.

Dependencies
------------

- `universe.unix.package_install`, to install the system packages.

Packages
--------

The below listed packages are installed by this role.

### Fedora

All packages from the Red Hat family plus the following:

- `dash` – A POSIX-compliant implementation of /bin/sh that aims to be as small
  as possible.

### Red Hat

- `acl` – The `getfacl` and `setfacl` utilities needed for manipulating access
  control lists.
- `attr` – A set of tools for manipulating extended attributes on filesystem
  objects.
- `bash-completion` – A collection of shell functions that take advantage of the
  programmable completion feature of bash.
- `bash` – The GNU Bourne Again shell (Bash).
- `bzip2` – A high quality data compressor.
- `chrony` – A versatile implementation of the Network Time Protocol (NTP).
- `cpio` – Copies files into or out of a `cpio` or `tar` archive.
- `cryptsetup` – A utility for setting up disk encryption using dm-crypt kernel
  module.
- `dhcp-client` – Allows individual devices on an IP network to get their own
  network configuration information.
- `grep` – Searches through textual input for lines which contain a match to a
  specified pattern.
- `gzip` – GNU gzip data compression program.
- `logrotate` – Utility designed to simplify the administration of log files.
- `man-pages` – A large collection of manual pages from the Linux Documentation
  Project (LDP).
- `openssh-server` – A program for logging into and executing commands on a
  remote machine.
- `parted` – Allows to create, destroy, resize, move, and copy hard disk
  partitions.
- `rng-tools` – A random number generator daemon and its tools.
- `sed` – Takes text as input, performs an operation or set of operations on
  the text and outputs the modified text.
- `tar` – The GNU tar program saves many files together in one archive.
- `vim` – An updated and improved version of the `vi` editor.
- `zsh` – A command interpreter usable as an interactive login shell and as a
  shell script command processor.
