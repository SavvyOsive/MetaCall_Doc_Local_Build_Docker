Installing MetaCall using ArchLinux AUR
========================================

Repository holding the package distribution of MetaCall for Arch User Repository - `Repo Link <https://github.com/metacall/aur>`_

`Here <https://github.com/metacall/aur>`_ is hosted the PKGBUILD script for the current Metacall CLI, it also inside the `AUR <https://aur.archlinux.org/packages/metacall-git>`_ under the name metacall-git.

The variable METACALL_LOADER_language=on can be set in order to build with support of a specific loader.

Supported loaders are found in the following documentation.

Using your favorite AUR helper you can install the package :

``paru``

.. code-block:: bash

    sudo paru -S metacall-git

``aura``

.. code-block:: bash

    sudo aura -Axc metacall-git
