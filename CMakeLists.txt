cmake_minimum_required(VERSION 3.0)
project(VectorizedBatchPIR)

# Build SEAL first
add_subdirectory(third_party/SEAL)

# Set the build directory
set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/build)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})

include_directories(header)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/third_party/SEAL/native/src)

# Set the output directory
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# Get all source files under src
file(GLOB_RECURSE SOURCES "src/*.cpp" "src/*.h")

# Create executable target and add source files
add_executable(vectorized_batch_pir ${SOURCES})

# Set include directories
target_include_directories(vectorized_batch_pir
    PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}
        ${CMAKE_CURRENT_SOURCE_DIR}/third_party/SEAL/native/src
)

# Set C++ standard
set_target_properties(vectorized_batch_pir PROPERTIES CXX_STANDARD 11)

# Link directly with seal
target_link_libraries(vectorized_batch_pir seal)

# Add compiler flags for optimization
if (CMAKE_CXX_COMPILER_ID MATCHES "GNU|Clang")
    target_compile_options(vectorized_batch_pir PRIVATE "-O3")
endif()
