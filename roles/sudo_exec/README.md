<!-- roles/sudo_exec/README.md
  -- =========================
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

universe.unix.sudo_exec
=======================

Purpose
-------

The `universe.unix.sudo_exec` role restricts the ability of the `sudo` command
to be executed. The role creates a new group where only users of this group have
the permission to run the `sudo` command.

Variables
---------

`sudo_exec_group` (Default: `"sudoexec"`)
: Name of the group providing execution permission of the `sudo` command.

`sudo_exec_user`
: Name of a user to be added to the sudo execution group. This variable can be a
list of users.
