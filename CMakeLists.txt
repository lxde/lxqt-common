cmake_minimum_required(VERSION 3.0.2 FATAL_ERROR)

project(lxqt-common)

set(LXQTBT_MINIMUM_VERSION "0.1.0")

find_package(lxqt-build-tools ${LXQTBT_MINIMUM_VERSION} REQUIRED)

include(GNUInstallDirs)
include(LXQtTranslateDesktop)
include(LXQtConfigVars)

install(DIRECTORY "graphics/" DESTINATION "${LXQT_GRAPHICS_DIR}")

# default config files
add_subdirectory(config)
add_subdirectory(autostart)

# xsession *.desktop file for display managers
add_subdirectory(xsession)
add_subdirectory(themes)
add_subdirectory(menu)
add_subdirectory(icons)
