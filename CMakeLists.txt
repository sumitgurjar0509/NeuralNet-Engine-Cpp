cmake_minimum_required(VERSION 3.10)

project(neuralnet_engine VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()

set(CMAKE_CXX_FLAGS_DEBUG "-g")
set(CMAKE_CXX_FLAGS_RELEASE "-O3")

include_directories(${PROJECT_SOURCE_DIR}/include)

file(GLOB TARGET_SRC
    ${PROJECT_SOURCE_DIR}/src/*.cpp
)

add_executable(neural_net ${TARGET_SRC})
