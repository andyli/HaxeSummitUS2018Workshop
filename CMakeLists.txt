cmake_minimum_required(VERSION 3.0)

project(Game C)

include_directories(
    hashlink/src
    bin/src
)

add_subdirectory(
    hashlink
)

add_executable(Game bin/src/main.c)

target_link_libraries(Game
    libhl
    fmt.hdll
    ui.hdll
)