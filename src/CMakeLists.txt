cmake_minimum_required(VERSION 3.22)

project(game_boy_emulator_client)

# ADD ALL CMAKE WITH SRC FILE
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/core)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/inc)

# INCLUDE PATH FOR SRC FILE
include(${CMAKE_CURRENT_LIST_DIR}/core/CMakeLists.txt)
include(${CMAKE_CURRENT_LIST_DIR}/inc/CMakeLists.txt)

# add_executable(${PROJECT_NAME} ${CORE})