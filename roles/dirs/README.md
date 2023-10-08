<!-- roles/dirs/README.md
  -- ====================
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

universe.unix.dirs
==================

Purpose
-------

Installation directories should always be named by variables, so it is easy
to install in a nonstandard place. The `universe.unix.dirs` role provides
installation directories so that other roles can use them to define the location
of the various files under their management.

The directories are based on a standard Unix file system layout as
specified by the [Filesystem Hierarchy Standard](
https://refspecs.linuxfoundation.org/fhs.shtml).

Emitted variables follow the [GNU Variables for Installation Directories](
https://www.gnu.org/prep/standards/html_node/Directory-Variables.html)
guideline.

Variables
---------

The role defines a number of variables for each installation directory.
Variables are prefixed, with each prefix providing a different information about
the installation directory.

The following prefixes are available:

- `dirs_*`, the actual installation directory value as configured from within
  Ansible.
- `dirs_env_*`, the value of the environment variable as set on the target
  host for the installation directory.
- `dirs_var_*`, name of the environment variable for the installation
  directory.

Use the above listed prefixes along with the installation directory name to
access the value of interest.

### Installation directories

`prefix`
: A prefix used in constructing the default values for other installation
directories.
`exec_prefix`
: A prefix used in constructing the default values for executable installation
directories.

`bindir`
: The directory for installing executable programs that users can run.
`datadir`
: The directory for installing idiosyncratic read-only architecture-independent
data files for this program.
`datarootdir`
: The root of the directory tree for read-only architecture-independent data
files.
`docdir`
: The directory for installing documentation files (other than Info or Man) for
the package.
`includedir`
: The directory for installing header files to be included by user programs with
the C ‘`#include`’ preprocessor directive.
`infodir`
: The directory for installing the Info files for this package.
`libexecdir`
: The directory for installing executable programs to be run by other programs
rather than by users.
`libdir`
: The directory for object files and libraries of object code.
`localstatedir`
: The directory for installing data files which the programs modify while they
run, and that pertain to one specific machine.
`mandir`
: The top-level directory for installing the man pages (if any) for this
package.
`runstatedir`
: The directory for installing data files which the programs modify while they
run, that pertain to one specific machine, and which need not persist longer
than the execution of the program.
`sbindir`
: The directory for installing executable programs that can be run from the
shell, but are only generally useful to system administrators.
`sharedstatedir`
: The directory for installing architecture-independent data files which the
programs modify while they run.
`sysconfdir`
: The directory for installing read-only data files that pertain to a single
machine–that is to say, files for configuring a host.
