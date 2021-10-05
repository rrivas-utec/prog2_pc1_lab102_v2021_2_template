cmake_minimum_required(VERSION 3.10.2)
project(prog2_pc1_lab102_v2021_2)

set(CMAKE_CXX_STANDARD 20)
if(UNIX AND NOT APPLE)
    SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pthread")
endif()

include_directories(./src)
file(GLOB source_files
        main.cpp
        src/*.h
        src/*.cpp)

add_executable(${PROJECT_NAME}
        ${source_files}
    )

add_subdirectory(autograder)

