<!-- roles/podman_install/README.md
  -- ==============================
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

universe.unix.podman_install
============================

Purpose
-------

The `universe.unix.podman_install` role installs [Podman](https://podman.io/), a
daemonless, open source, Linux native tool designed to make it easy to find,
run, build, share and deploy applications using Open Containers Initiative (OCI)
Containers and Container Images.

Dependencies
------------

This role depends on the following roles:

`universe.unix.dirs`
: To get installation directories of the system.

`universe.unix.package_install`
: To install the system packages required for this role.

Variables
---------

`podman_install_create_user` (Default: `false`)
: Whether or not to create a dedicated user to run containers with no administrative privileges.

`podman_install_enable_system_service` (Default: `false`)
: Whether or not to enable the system's Podman API for remote access.

`podman_install_enable_user_service` (Default: `false`)
: Whether or not to enable the user's Podman API for remote access..

`podman_install_user_group` (Default:
`"{{ podman_install_user_name }}"`)
: Primary group of the user specifically created to run Podman in rootless mode.

`podman_install_user_home` (Default:
`"{{ dirs_sharedstatedir }}/{{ podman_install_user_name }}"`)
: Home directory of the Podman user.

`podman_install_user_name` (Default: `"podman"`)
: Name of the user specifically created to run Podman in rootless mode.

`podman_install_user_subid_count` (Default: `65535`)
: Number of subordinate user/group IDs that are allocated to the Podman user.

`podman_install_user_subid_start` (Default: `1000000`)
: First subordinate user/group IDs that the Podman user is allowed to use.
