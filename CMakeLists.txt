cmake_minimum_required(VERSION 3.15)
project(buildTest VERSION 1.0 LANGUAGES CXX)

# Use C++14
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Export compile commands for clang-tidy
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Put runtime binaries into a predictable folder inside CMake binary dir
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# Main executable
add_executable(buildTest buildTest/Main.cpp)

# Testing (optional)
include(CTest)
enable_testing()