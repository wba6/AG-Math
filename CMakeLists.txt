cmake_minimum_required(VERSION 3.16)

#set the project name and version
project(AG-Math-Tests VERSION 1.0)

#specify the c++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Source files
file(GLOB_RECURSE libSrc
        ${PROJECT_SOURCE_DIR}/tests/*.c
        ${PROJECT_SOURCE_DIR}/tests/*.cpp
    )

# Add source header files
file(GLOB_RECURSE libHead
        ${PROJECT_SOURCE_DIR}/*.h
        ${PROJECT_SOURCE_DIR}/*.hpp
    )

add_executable(AG-Math-Tests ${libSrc} ${libHead})