.. roles/adp_package_install/README.rst
.. ====================================
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
universe.unix.apt_package_install
=================================

The ``universe.unix.apt_package_install`` role uses the `APT
<https://en.wikipedia.org/wiki/APT_(software)>`_ software package
manager to install package on the system.

Once the package installed, the role checks for configuration files marked with
``.dpkg-new`` or ``.dpkg-old``. The administrator can decide on the action to
take when such file is encountered.


Variables
---------

``package_install``
    A single package or a list of packages to be installed.

``package_install_config_keep``
    The action to take when a handling new configuration files.

    When set to ``new``, files marked with ``.dpkg-new`` will replace the existing
    file and files marked with ``.dpkg-old`` are deleted.

    When set to ``old``, files marked with ``.dpkg-old`` will replace the newly
    installed file and files marked with ``.dpkg-new`` are deleted.

``package_install_config_search`` (Default: ``["/etc", "/usr", "/var"]``)
    A list of folder within which to search for potential configuration files
    marked marked by the package installer.


Events
------

``system_package_installed``
    Triggered after a successful package installation.
