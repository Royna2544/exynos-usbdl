cmake_minimum_required(VERSION 3.14)
project(exynos-usbdl LANGUAGES C)

find_package(PkgConfig REQUIRED)
pkg_check_modules(LIBUSB REQUIRED IMPORTED_TARGET libusb-1.0)

add_executable(exynos-usbdl exynos-usbdl.c)
target_link_libraries(exynos-usbdl PRIVATE PkgConfig::LIBUSB)
