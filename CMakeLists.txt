cmake_minimum_required(VERSION 3.5)

project(Visualization LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)

add_executable(Visualization main.cpp)
target_link_directories(Visualization PRIVATE  OpenGL::GL)
target_link_libraries(Visualization -lglfw -lGL -lGLEW GLEW::GLEW )
