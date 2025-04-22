cmake_minimum_required(VERSION 3.10)
project(Algorithms)

# Set the C++ standard to C++14
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add the source files
add_executable(${PROJECT_NAME} ./main.cpp)

# Add the algorithm source files
add_subdirectory(src)

# Add the utility source files
#add_subdirectory(utils)

# Add the test source files
#add_subdirectory(tests)

# Link the executable to the algorithm and utility libraries
#target_link_libraries(${PROJECT_NAME} algorithms utils)

# Install the executable
install(TARGETS ${PROJECT_NAME} DESTINATION bin)

# Add include directories for the algorithms and utils
set(CMAKE_CXX_INCLUDE_DIRECTORIES ${CMAKE_CXX_INCLUDE_DIRECTORIES} include/algorithms)
#set(CMAKE_CXX_INCLUDE_DIRECTORIES ${CMAKE_CXX_INCLUDE_DIRECTORIES} include\utils)

# Install the header files
install(DIRECTORY include/ DESTINATION include)