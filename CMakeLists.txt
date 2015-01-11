cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(MagneticMesh)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${PROJECT_SOURCE_DIR}/cmake/Modules/")
find_package(Leap REQUIRED)

include_directories(${LEAP_INCLUDE_DIRS})

include_directories(
    ${PROJECT_SOURCE_DIR}/src
)

add_executable (MagneticMesh
    src/HandController.cpp
    src/HandController.h
    src/MagneticMesh.cpp
    src/MagneticMesh.h
)

target_link_libraries (MagneticMesh ${LEAP_LIBRARIES} -lz)
