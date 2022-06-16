cmake_minimum_required(VERSION 3.10)

project(Example)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

#
set(BUILD_SHARED_LIBS OFF CACHE BOOL "Build shared libraries")
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "Build the GLFW example programs")
set(GLFW_BUILD_TESTS OFF CACHE BOOL "Build the GLFW test programs")
set(GLFW_BUILD_DOCS OFF CACHE BOOL "Build the GLFW documentation")
set(GLFW_INSTALL OFF CACHE BOOL "Generate installation target")
set(GLFW_VULKAN_STATIC OFF CACHE BOOL "Assume the Vulkan loader is linked with the application")

message(" ${PROJECT_BINARY_DIR} ala ${PROJECT_SOURCE_DIR} using ${CMAKE_CXX_COMPILER_ID}")

set(GLFW ${PROJECT_SOURCE_DIR}/deps/glfw-3.3.7)
set(GLAD ${PROJECT_SOURCE_DIR}/deps/glad)

add_subdirectory(${GLFW})
#add_subdirectory(${GLAD})

add_subdirectory(example)
