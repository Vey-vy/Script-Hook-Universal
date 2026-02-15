cmake_minimum_required(VERSION 3.11)

project(ScriptHook)

set(SRC_DIR "${PROJECT_SOURCE_DIR}/src")

include(CheckIncludeFileCXX)

set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_REQUIRED_QUIET ON)

set(OK TRUE)

file(GLOB_RECURSE HEADERS "src/**.hpp")
file(GLOB_RECURSE SRC_MAIN "src/**.cpp")
source_group(FILES ${SRC_MAIN})
add_library(ScriptHook MODULE "${SRC_MAIN}")

add_compile_definitions(_CRT_SECURE_NO_WARNINGS)

message(STATUS "")
 
target_include_directories(ScriptHook PRIVATE 
    "${SRC_DIR}"
)

if(NOT OK)
    file(READ "${CMAKE_CURRENT_BINARY_DIR}/CMakeFiles/CMakeError.log" LOG)
    message(STATUS ${LOG})
endif()

