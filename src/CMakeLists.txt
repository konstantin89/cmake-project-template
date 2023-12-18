cmake_minimum_required(VERSION 3.0)

file(GLOB APP_SOURCES ${CMAKE_CURRENT_LIST_DIR}/*.cpp)
set(APP_NAME AppName)

add_executable(${APP_NAME} ${APP_SOURCES})

set(AGENT_INCLUDE_PATHS     
    ${ROOT_INCLUDE_DIRECTORY}
    ${CMAKE_CURRENT_LIST_DIR})  
 
target_include_directories(${APP_NAME} PRIVATE ${AGENT_INCLUDE_PATHS})
