cmake_minimum_required(VERSION 3.10)

add_executable(Example hello_triangle_indexed.cpp ${GLAD}/src/glad.c)
target_include_directories(Example PUBLIC ${GLFW}/include)
target_include_directories(Example PUBLIC ${GLAD}/include)
target_link_libraries(Example PUBLIC glfw)