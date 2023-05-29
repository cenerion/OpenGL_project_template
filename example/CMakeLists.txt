cmake_minimum_required(VERSION 3.10)

add_executable(Example hello_triangle_indexed.cpp)
target_link_libraries(Example PUBLIC glfw libglew_static)
