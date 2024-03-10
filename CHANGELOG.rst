.. CHANGELOG.rst
.. =============
..
.. Copying
.. -------
..
.. Copyright (c) 2022 universe.unix authors and contributors.
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

===========================
universe.unix Release Notes
===========================

.. contents:: Topics


v0.3.0
======

Release Summary
---------------

Package groups installation.

Major Changes
-------------

- package_install_core - Add a new role to install the bare minimum list
  of packages required for a pleasant operating system experience.
- package_install_hwutils - Add a new role to install a set of utilities
  to manage bare-metal systems.
- package_install_netutils - Add a new role to install a set of network
  related utilities.
- package_install_utils - Add a new role to install a set of system
  utilities to improve the usage experience.

v0.2.0
======

Release Summary
---------------

Few fixes.

Minor Changes
-------------

- package_install - Add the variable ``package_install_state`` to
  specify the installation state of a package.

v0.1.0
======

Release Summary
---------------

First release of the ``universe.unix`` collection. Everything
must be considered early stage and no yet ready for production.
