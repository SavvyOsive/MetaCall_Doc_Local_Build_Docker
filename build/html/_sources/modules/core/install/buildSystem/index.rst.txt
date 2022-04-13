Building And Installing MetaCall
====================================

Follow these steps to build and install METACALL manually.

.. code-block:: bash

    git clone https://github.com/metacall/core.git
    mkdir core/build && cd core/build
    cmake ..

    # Unix (Linux and MacOs)
    sudo HOME="$HOME" cmake --build . --target install

    # Windows (or when installing to a path with permissions)
    cmake --build . --target install

Build Options
----------------

These options can be set using -D prefix when configuring CMake. For example, the following configuration enables the build of Python and Ruby loaders.

.. code-block:: bash

    cmake -DOPTION_BUILD_LOADERS_PY=On -DOPTION_BUILD_LOADERS_RB=On ..

Available build options are the following ones.

.. list-table:: Build Options
   :widths: 25 25 50
   :header-rows: 1

   * - ``Build Option``
     - ``Description``
     - ``Default Value``
   * - BUILD_SHARED_LIBS
     - Build shared instead of static libraries.
     - ON
   * - OPTION_SELF_CONTAINED
     - Create a self-contained install with all dependencies.
     - OFF
   * - OPTION_BUILD_TESTS
     - Build tests.
     - ON
   * - OPTION_BUILD_BENCHMARKS
     - Build benchmarks.
     - OFF
   * - OPTION_BUILD_DOCS
     - Build documentation.
     - OFF
   * - OPTION_BUILD_EXAMPLES
     - Build examples.
     - ON
   * - OPTION_BUILD_LOADERS
     - Build loaders.
     - ON
   * - OPTION_BUILD_SCRIPTS
     - Build scripts.
     - ON
   * - OPTION_BUILD_SERIALS
     - Build serials.
     - ON
   * - OPTION_BUILD_DETOURS
     - Build detours.
     - ON
   * - OPTION_BUILD_PORTS
     - Build ports.
     - OFF
   * - OPTION_FORK_SAFE
     - Enable fork safety.
     - OFF
   * - OPTION_THREAD_SAFE
     - Enable thread safety.
     - OFF
   * - OPTION_COVERAGE
     - Enable coverage.
     - OFF
   * - CMAKE_BUILD_TYPE
     - Define the type of build.
     - Release


Coverage
----------------

Debugging
------------

Build on Cloud - Gitpod
---------------------------



