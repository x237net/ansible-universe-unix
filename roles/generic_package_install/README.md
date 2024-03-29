<!-- roles/generic_package_install/README.md
  -- =======================================
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

universe.unix.generic_package_install
=====================================

Purpose
-------

The `universe.unix.generic_pkg_install` role uses the [ansible.builtin.package](
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/package_module.html#ansible-collections-ansible-builtin-package-module)
module to install a package on the system using its default package manager.

Variables
---------

`package_install`
: A single package or a list of packages to be installed.

`package_install_state` (Default: `"present"`)
: Whether to install (``present``), or remove (``absent``) a package. You can
use other states like ``latest`` ONLY if they are supported by the underlying
package module(s) executed.

Events
------

`system_package_installed`
: Triggered after a successful package installation.
