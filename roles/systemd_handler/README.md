<!-- roles/systemd_handler/README.md
  -- ===============================
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

universe.unix.systemd_handler
=============================

Purpose
-------

The `universe.unix.systemd_handler` role provides Ansible handlers to manage
systemd units and manager configuration.

Handlers
--------

`universe.unix.systemd_handler:deamon_reload`
: Reloads the systemd manager configuration. This re-runs all generators,
reloads all unit files, and recreates the entire dependency tree. While the
daemon is reloading, all sockets systemd listens on on behalf of user
configuration remain accessible. This is useful after creating or modifying unit
files.

`universe.unix.systemd_handler:disable`
: Disables the specified unit. Note that disabling a unit does not stop the
service if it is currently running.

`universe.unix.systemd_handler:enable`
: Enables the specified unit to start automatically at boot. Note that enabling
a unit does not start it in the current session.

`universe.unix.systemd_handler:reload`
: Reloads the specified unit's service-specific configuration. This requests the
service to reload its configuration files (typically via a `SIGHUP` or
service-specific reload command) without stopping or restarting the processes.

`universe.unix.systemd_handler:restart`
: Restarts the specified unit. This stops the active service and starts it
again. If the unit is not already running, it will be started.

`universe.unix.systemd_handler:start`
: Starts (activates) the specified unit. If the unit is already running, this
has no effect.

`universe.unix.systemd_handler:stop`
: Stops (deactivates) the specified unit. This terminates the processes
associated with the service.
