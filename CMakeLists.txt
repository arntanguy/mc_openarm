cmake_minimum_required(VERSION 3.21)

set(CXX_DISABLE_WERROR 1)
set(CMAKE_CXX_STANDARD 17)

set(PROJECT_NAME mc_openarm)
set(PROJECT_DESCRIPTION "OpenArm robot module for mc_rtc")

project(
  ${PROJECT_NAME}
  LANGUAGES CXX
  VERSION 1.0.0)

find_package(mc_rtc REQUIRED)

find_description_package(openarm_description)
set(MC_OPENARM_DESCRIPTION_PATH "${OPENARM_DESCRIPTION_PATH}")

add_subdirectory(src)
