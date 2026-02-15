cmake_minimum_required(VERSION 3.11)

project(ScriptHook)

set(SRC_DIR "${PROJECT_SOURCE_DIR}/src")

include(CheckIncludeFileCXX)

set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_REQUIRED_QUIET ON)

set(OK TRUE)

if(CMAKE_SIZEOF_VOID_P EQUAL 8)
    add_compile_definitions(FORCE_X64=1)
    message(STATUS "Architecture detected: 64-bit")
elseif(CMAKE_SIZEOF_VOID_P EQUAL 4)
    add_compile_definitions(FORCE_X32=1)
    message(STATUS "Architecture detected: 32-bit")
else()
    message(WARNING "Unknown architecture")
endif()

if(DEFINED TARGET_GAME)
    if(TARGET_GAME STREQUAL "GTAV")
        add_compile_definitions(TARGET_GTAV=1)
        message(STATUS "Target game: GTA V")
    elseif(TARGET_GAME STREQUAL "RDR2")
        add_compile_definitions(TARGET_RDR2=1)
        message(STATUS "Target game: Red Dead Redemption 2")
    elseif(TARGET_GAME STREQUAL "RDR")
        add_compile_definitions(TARGET_RDR=1)
        message(STATUS "Target game: Red Dead Redemption")
    elseif(TARGET_GAME STREQUAL "MP3")
        add_compile_definitions(TARGET_MP3=1)
        message(STATUS "Target game: Max Payne 3")
    endif()
endif()

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