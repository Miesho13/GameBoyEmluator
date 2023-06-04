cmake_minimum_required(VERSION 3.22)

# PROJECT CNF
set(This gameBoytEmulator)
project(${This})

set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)


# ON CTEST
enable_testing()

# ADD GOOGLE TEST TO PROJETC
add_subdirectory(googletest)

# RUN CMAKE FOR SRC PROJECT
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/src)

# MAKE STATIC LIB FOR PROJECT
include(${CMAKE_CURRENT_LIST_DIR}/src/core/CMakeLists.txt)
include(${CMAKE_CURRENT_LIST_DIR}/src/inc/CMakeLists.txt)
add_library(${This} STATIC ${core} ${inc})


# RUN TEST DEPENDENCIES
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/test) 