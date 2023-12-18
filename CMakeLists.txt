cmake_minimum_required(VERSION 3.0)

set(ProjectName "Project name")

project(${ProjectName})

set(CMAKE_BUILD_TYPE Debug)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CATCH2_PATH ${CMAKE_CURRENT_LIST_DIR}/submodules/Catch2)
set(CATCH2_INCLUDE_DIRECTORY ${CATCH2_PATH}/submodules/Catch2/src)
add_subdirectory(${CATCH2_PATH})

set (ROOT_INCLUDE_DIRECTORY ${CMAKE_CURRENT_LIST_DIR}/.)

add_subdirectory(./src)
add_subdirectory(./tests)