<!-- roles/systemd_unit/README.md
  -- ============================
  --
  -- Copying
  -- -------
  --
  -- Copyright (c) 2026 universe.unix authors and contributors.
  --
  -- This file is part of the *universe.unix* project.
  --
  -- *universe.unix* is a free software project. You can redistribute it
  -- and/or modify it following the terms of the MIT License.
  --
  -- This software project is distributed *as is*, WITHOUT WARRANTY OF ANY KIND;
  -- including but not limited to the WARRANTIES OF MERCHANTABILITY, FITNESS FOR
  -- A PARTICULAR PURPOSE and NONINFRINGEMENT.
  --
  -- You should have received a copy of the MIT License along with
  -- *universe.unix*. If not, see <http://opensource.org/licenses/MIT>.
  -->

universe.unix.systemd_unit
==========================

Purpose
-------

The `universe.unix.systemd_unit` role provides tasks to deploy and manage
systemd unit files (such as services, sockets, timers, or mounts). It supports
installing units for both system-wide and user-specific sessions, automatically
handling correct installation paths, file ownership, permissions, and SELinux
contexts.

Variables
---------

`systemd_unit_name`
: The name of the systemd unit file to create (e.g., `application.service`,
`application.timer`). This variable is mandatory.

`systemd_unit_content`
: The plain text content of the systemd unit file. This variable is mandatory.

`systemd_unit_scope` (Default: `"system"`)
: The session scope for the systemd unit. This variable is optional and defaults
to `system`. Supported scopes are:

- `system`: Installs a system-wide service unit in
  `{{ dirs_prefix }}/lib/systemd/system`.
- `global`: Installs a global user service unit in
  `{{ dirs_prefix }}/lib/systemd/user` (accessible by all users' sessions).
- `user`: Installs a user-specific service unit in the current user's XDG data
  directory (`{{ dirs_xdg_data_home }}/systemd/user`, resolving to
  `~/.local/share/systemd/user`).

Notifications
-------------

This role automatically notifies the
`universe.unix.systemd_handler:daemon_reload` handler when a unit file is
created or updated, ensuring systemd manager configuration is reloaded for the
appropriate session scope.
