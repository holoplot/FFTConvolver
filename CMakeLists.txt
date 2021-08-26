cmake_minimum_required(VERSION 3.16)
project(fftconvolver)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(${PROJECT_NAME} "")

target_sources(${PROJECT_NAME} PRIVATE
    AudioFFT.h
    FFTConvolver.h
    TwoStageFFTConvolver.h
    Utilities.h
    
    AudioFFT.cpp
    FFTConvolver.cpp
    TwoStageFFTConvolver.cpp
    Utilities.cpp
)

target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_LIST_DIR})

add_subdirectory(test)
