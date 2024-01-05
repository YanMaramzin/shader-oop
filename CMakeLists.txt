cmake_minimum_required(VERSION 3.27)
project(graph_template)

set(CMAKE_CXX_STANDARD 17)

add_executable(graph_template main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(share/glfw)
target_link_libraries(${PROJECT_NAME} glfw)

add_subdirectory(share/glad)
target_link_libraries(${PROJECT_NAME} glad)