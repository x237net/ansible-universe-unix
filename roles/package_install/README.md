<!-- roles/package_install/README.md
  -- ===============================
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

universe.unix.package_install
=============================

Purpose
-------

The `universe.unix.package_install` role is a meta role which will call the
package installation role which is appropriate to the underlying system:

- `universe.unix.apt_package_install`, for Debian based systems;
- `universe.unix.dnf_package_install`, for Red Hat based systems.

On last resort, the `universe.unix.generic_package_install` role is called.

Variables
---------

`package_install`
: A single package or a list of packages to be installed.

`package_install_config_keep`
: If the underlying role is supporting this variable, specifies the action to
take when handling configuration files. When set to `new`, configuration files
coming from the newly installed package will replace the existing configuration
file. When set to `old`, existing configuration files are kept and any new
configuration file from the installed package is ignored.

`package_install_config_search` (Default: `["/etc", "/usr", "/var"]`)
: A list of folder within which to search for potential configuration files
marked marked by the package installer.

Events
------

`system_package_installed`
: Triggered after a successful installation of a package.
