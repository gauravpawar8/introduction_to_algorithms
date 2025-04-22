cmake_minimum_required(VERSION 3.10)
project(Algorithms)

# Set the include directory
include_directories(include)

# Add the src directory
add_subdirectory(src)

# Add the main.cpp file
add_executable(${PROJECT_NAME} main.cpp)