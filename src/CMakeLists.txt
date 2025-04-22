# src/algorithms/CMakeLists.txt

# Set the include directory for this folder
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

# Add source files for algorithms
set(ALGORITHMS_SOURCES
  algorithms/sorting/insertion_sort.cpp
)

# Add headers for algorithms
set(ALGORITHMS_HEADERS
  algorithms/sorting/insertion_sort.h
)

# Create a library for algorithms
add_library(algorithms STATIC ${ALGORITHMS_SOURCES})

# Add include directories for algorithms library
target_include_directories(algorithms PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# Install headers for algorithms library
install(FILES ${ALGORITHMS_HEADERS} DESTINATION include/algorithms)