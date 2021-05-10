# Argparse Library Debian Package

[![latest release](https://img.shields.io/github/v/release/threeal/libargparse-deb)](https://github.com/threeal/libargparse-deb/releases)
[![repository size](https://img.shields.io/github/repo-size/threeal/libargparse-deb)](https://github.com/threeal/libargparse-deb/pulse)
[![license](https://img.shields.io/github/license/threeal/libargparse-deb)](./LICENSE)

This project contains a [CPack](https://cmake.org/cmake/help/latest/module/CPack.html) build workspace of the [Argparse](https://github.com/p-ranav/argparse) library.
This project is created to simplify the deployment of the library as a [Debian package](https://wiki.debian.org/Packaging).

## Usage

### Updating the Source Code

- Initialize the submodule and pull the latest commits.
  ```bash
  $ git submodule update --init --recursive
  ```
- Modify the CPack configuration in the [CMakeLists.txt](./CMakeLists.txt) according to the current source code information.
  > See [this guide](https://cmake.org/cmake/help/latest/cpack_gen/deb.html) for more information on CPack configuration for Debian package.

### Building the Project

- Create a build directory and move to it.
  ```bash
  $ mkdir build
  $ cd build
  ```
- Configure the CMake with the following options.
  ```bash
  $ cmake -DCMAKE_INSTALL_PREFIX=/usr ..
  ```
- Build the project.
  ```bash
  $ make
  ```
  > Optionally, you could speed up the build process by specifying the parallel job using `-j` option, see [this](https://www.gnu.org/software/make/manual/html_node/Parallel.html).
- Create the Debian package using CPack.
  ```bash
  $ cpack
  ```

## License

This project is maintained by [Alfi Maulana](https://threeal.github.io/) and licensed under the [MIT LICENSE](./LICENSE)
