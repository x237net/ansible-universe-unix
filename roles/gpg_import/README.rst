.. roles/gpg_import/README.rst
.. ===========================
..
.. Copying
.. -------
..
.. Copyright (c) 2023 universe.unix authors and contributors.
..
.. This file is part of the *universe.unix* project.
..
.. *universe.unix* is a free software project. You can redistribute it and/or
.. modify it following the terms of the MIT License.
..
.. This software project is distributed *as is*, WITHOUT WARRANTY OF ANY KIND;
.. including but not limited to the WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
.. PARTICULAR PURPOSE and NONINFRINGEMENT.
..
.. You should have received a copy of the MIT License along with
.. *universe.unix*. If not, see <http://opensource.org/licenses/MIT>.
..
universe.unix.gpg_import
========================

Purpose
-------

The ``universe.unix.gpg_import`` role adds a new key into the system's (root)
keyring.


Dependencies
------------

This role depends on the following roles:

``universe.unix.gpg_install``
    To install OpenPGP key management utilities on the system.


Variables
---------

The role exposes the following variables for its configuration:

``gpg_import_content``
    Content of the key to be added to the keyring.
