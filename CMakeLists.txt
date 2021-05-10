cmake_minimum_required(VERSION 3.10)

add_subdirectory("argparse")

set(CPACK_GENERATOR "DEB")
set(CPACK_DEBIAN_FILE_NAME DEB-DEFAULT)

set(CPACK_DEBIAN_PACKAGE_NAME "libargparse-dev")

set(CPACK_DEBIAN_PACKAGE_VERSION 2.1.0)
set(CPACK_DEBIAN_PACKAGE_RELEASE 1)

set(CPACK_DEBIAN_PACKAGE_DESCRIPTION "Argument Parser for Modern C++")

set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Alfi Maulana <alfi.maulana.f@gmail.com>")
set(CPACK_DEBIAN_PACKAGE_HOMEPAGE "https://github.com/p-ranav/argparse")

set(CPACK_DEBIAN_PACKAGE_DEPENDS "libc6, libgcc-s1, libstdc++6")

include(CPack)
