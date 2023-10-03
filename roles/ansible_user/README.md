<!-- roles/ansible_user/README.md
  -- ============================
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

universe.unix.ansible_user
==========================

Purpose
-------

The `universe.unix.ansible_user` role make sure that a user is properly setup
on the host for it to be managed by Ansible.

Upon creation of the Ansible user, the `universe.unix.ssh_authorized_key` role
is called to assign public SSH keys to the user. Therefore, variables allowed by
this role must also be provided.

Variables
---------

The role exposes the following variables for its configuration:

`ansible_user_become_sudo` (Default: `true`)
: Should the Ansible user make use of `sudo` to gain administrative rights?

`ansible_user_home_basedir` (Default: `/var/lib`)
: A path prefix used in constructing the user's home directory.

`ansible_user_name` (Default: `ansible`)
: Name of the user which will be used by Ansible to manage the host.

`ansible_user_group` (Default: `ansible`)
: Name of the main group of the Ansible user.

`ansible_user_sudo_exec` (Default: `true`)
: Should execution of the `sudo` command be restricted to a specific group?
