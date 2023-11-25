#cmake_minimum_required(VERSION 3.17)
#project(sdlTest)
#
#find_package(SDL2 REQUIRED)
#find_package(GLM REQUIRED)
#
#include_directories(${SDL2_INCLUDE_DIRS} ${GLM_INCLUDE_DIRS})
#
#add_executable(sdlTest main.cpp)
#
#target_link_libraries(sdlTest ${SDL2_LIBRARIES})

cmake_minimum_required(VERSION 3.17)
project(sdlTest)

find_package(SDL2 REQUIRED)

# Specify the path to the GLM headers
set(GLM_INCLUDE_DIRS "${CMAKE_SOURCE_DIR}/glm")

include_directories(${SDL2_INCLUDE_DIRS} ${GLM_INCLUDE_DIRS})

add_executable(sdlTest main.cpp)

target_link_libraries(sdlTest PRIVATE ${SDL2_LIBRARIES})


