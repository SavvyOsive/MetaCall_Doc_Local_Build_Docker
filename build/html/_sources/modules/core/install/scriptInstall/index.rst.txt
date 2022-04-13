Installing MetaCall Using Shell Script
========================================

Cross-platform set of scripts to install MetaCall Core infrastructure.


The following scripts are provided in order to install MetaCall:

* `install.sh <https://raw.githubusercontent.com/metacall/install/master/install.sh>`_  ``bash or zsh | Linux or MacOS``

* `install.ps1 <https://raw.githubusercontent.com/metacall/install/master/install.ps1>`_ ``PowerShell | Windows``


In order to install MetaCall in one line, curl or wget or powershell can be used:

*  curl:

.. code-block:: bash

    curl -sL https://raw.githubusercontent.com/metacall/install/master/install.sh | sh

*  wget:

.. code-block:: bash

    wget -O - https://raw.githubusercontent.com/metacall/install/master/install.sh | sh

*  powershell:

.. code-block:: bash

    powershell -NoProfile -ExecutionPolicy unrestricted -Command "[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; &([scriptblock]::Create((Invoke-WebRequest -UseBasicParsing 'https://raw.githubusercontent.com/metacall/install/master/install.ps1')))"

Installing on Linux or MacOS
------------------------------

Additional parameters for the install script:

*     ``--update:`` Updates automatically MetaCall if it is already installed without asking to the user.
*     ``--uninstall:`` Uninstalls MetaCall if it is already installed without asking to the user. Overwrites the update command.
*     ``--docker-install:`` Runs Docker installation overwriting Docker fallback option over binary installation.
*     ``--no-check-certificate:`` When running binary installation (the default one), disables checking certificates when downloading the tarball. Useful for environments where there is not certificates, but insecure.
*     ``--no-docker-fallback:`` When running binary installation (the default one), disables Docker installation as fallback if the binary installation fails.
*     ``--from-path <path>:`` Installs MetaCall from specific path, the <path> points to a previously download tarball located in your file system.

Example usage:

*   Install with curl without checking certificates and without docker fallback:

.. code-block:: bash

    curl --insecure -sL https://raw.githubusercontent.com/metacall/install/master/install.sh | sh -s -- --no-check-certificate --no-docker-fallback

*   Install with wget using Docker installer:

.. code-block:: bash

    wget -O - https://raw.githubusercontent.com/metacall/install/master/install.sh | sh -s -- --docker-install

*   Install with wget from a existing tarball located at /root/downloads/metacall-tarball-linux-amd64.tar.gz:

.. code-block:: bash

    wget -O - https://raw.githubusercontent.com/metacall/install/master/install.sh | sh -s -- --from-path /root/downloads/metacall-tarball-linux-amd64.tar.gz

*   Install MetaCall in a BusyBox without certificates:

.. code-block:: bash

    wget --no-check-certificate -O - https://raw.githubusercontent.com/metacall/install/master/install.sh | sh -s -- --no-check-certificate

Installing on Windows
-----------------------

Additional parameters for the install script:

*   ``-InstallDir <directory>:`` Defines a custom folder in order to install MetaCall in, otherwise it uses %LocalAppData%\MetaCall by default.
*   ``-Version <version>:`` Version of the tarball to be downloaded. Versions are available here. Uses latest version by default.

Example usage:

*   Install tarball version v0.1.0 into D:\metacall:

.. code-block:: bash

    powershell -NoProfile -ExecutionPolicy unrestricted -Command "[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; &([scriptblock]::Create((Invoke-WebRequest -UseBasicParsing 'https://raw.githubusercontent.com/metacall/install/master/install.ps1'))) -InstallDir 'D:\metacall' -Version '0.1.0'"

Testing
---------------------

Refer to `repo <https://github.com/metacall/install>`_

.. code-block:: bash

    ./test.sh
