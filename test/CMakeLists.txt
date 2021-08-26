cmake_minimum_required(VERSION 3.16)
project(fftconvolver-test)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(${PROJECT_NAME} "")

target_sources(${PROJECT_NAME} PRIVATE
    Test.cpp
)

target_link_libraries(${PROJECT_NAME} PRIVATE fftconvolver)
