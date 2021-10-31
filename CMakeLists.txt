cmake_minimum_required(VERSION 3.0.0)
project(graphics VERSION 0.1.0)

set(CMAKE_APPLE_SILICON_PROCESSOR)

INCLUDE_DIRECTORIES(
    /Users/keki/vcpkg/installed/arm64-osx/include
)
LINK_DIRECTORIES(
    /Users/keki/vcpkg/installed/arm64-osx/lib
) 

add_executable(graphics main.cpp)

find_package(SDL2 CONFIG REQUIRED)
target_link_libraries(graphics PRIVATE SDL2::SDL2 SDL2::SDL2main SDL2::SDL2-static)