cmake_minimum_required(VERSION 3.10)

# Project name and version
project(introduction_to_algorithms VERSION 1.0)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Include header files
include_directories(include)

# Add source files
file(GLOB_RECURSE SOURCES "src/*.cpp")

# Add the executable
add_executable(introduction_to_algorithms main.cpp ${SOURCES})
