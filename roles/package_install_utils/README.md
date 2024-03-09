<!-- roles/package_install_utils/README.md
  -- =====================================
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

universe.unix.package_install_utils
===================================

Purpose
-------

The `universe.unix.package_install_utils` role installs a set of system
utilities to improve the usage experience.

Dependencies
------------

- `universe.unix.package_install`, to install the system packages.

Packages
--------

The below listed packages are installed by this role.

### Fedora

All packages from the Red Hat family plus the following:

- `htop` – An interactive text-mode process viewer for Linux, similar to `top`.

### Red Hat

- `bc` – Includes `bc` and `dc`. `bc` is an arbitrary precision numeric
  processing arithmetic language. `dc` is an interactive arbitrary precision
  stack based calculator, which can be used as a text mode calculator.
- `binutils` – A collection of binary processing utilities.
- `diffutils` – A set of utilities to compare files and shows the differences.
- `dos2unix` – Convert text files with DOS or Mac line endings to Unix line
  endings and vice versa.
- `file` – Used to identify a particular file according to the type of data
  contained by the file.
- `findutils` – Programs which help to locate files on the system.
- `gnupg2` – A tool for secure communication and data storage.
- `iotop` – A program with a top like UI used to show of behalf of which process
  is the I/O going on.
- `jq` – A lightweight and flexible command-line JSON processor.
- `lsof` – List information about files that are open by the processes running
  on a UNIX system.
- `patchutils` – Collection of programs that can manipulate patch files in a
  variety of ways.
- `symlinks` – Utility to perform maintenance on symbolic links.
- `tmux` – Enable a number of terminals to be accessed and controlled from a
  single terminal.
- `tree` – Utility to display recursively the contents of directories in a
  tree-like format.
- `unzip` – Utility is used to list, test, or extract files from a Zip archive.
- `which` – Show the full pathname of a specified program, if the specified
  program is in the `PATH` variable.
- `xz` – Utilities to make LZMA compression similar to use than other existing
  compression algorithms.
- `zip` – A compression and file packaging utility of the Zip format.
