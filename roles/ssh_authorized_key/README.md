<!-- roles/ssh_authorized_key/README.md
  -- ==================================
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

universe.unix.ssh_authorized_key
================================

Purpose
-------

The `universe.unix.ssh_authorized_key` role manages the SSH's [authorized keys](
https://www.ssh.com/academy/ssh/authorized-keys-openssh) file for a given user.

Authorized keys specify which users are allowed to log into a system using
public key authentication in SSH.

Variables
---------

`ssh_authorized_keys` – **list**
: A list of public SSH keys to be authorized. Each key is a dictionary
allowing the following keys:

- `key` – **string**, the SSH public key to be authorized;
- `comment` – **string**, the comment to be prepended to the key;
- `options` – **string**, SSH key [options](
https://www.ssh.com/academy/ssh/authorized-keys-openssh#format-of-the-authorized-keys-file)
to be prepended to the key.

`ssh_authorized_key_user` – **string**
: Name of the user for which to manage the SSH authorized keys.

`ssh_authorized_key_exclusive` – **bool** (Default: `false`)
: When `true`, only the specified keys are authorized for the user, when
`false`, the provided keys are appended to the list of authorized keys.

`ssh_authorized_key_path` – **string** (Default: `null`)
: Path to the SSH key authorization file.

`ssh_authorized_key_state` – **string** (Default: `"present"`)
: Whether the provided keys should be added or removed to the file.
