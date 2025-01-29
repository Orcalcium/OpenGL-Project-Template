cmake_minimum_required(VERSION 3.10)
project(project)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the main.cpp file to the project
add_executable(project ./code/main.cpp ./include/glad/glad.c)

# Specify the path to the installed GLFW library
set(GLFW_DIR "./include/GLFW/install/lib/cmake/glfw3")

# Find the GLFW package 
find_package(glfw3 REQUIRED PATHS ${GLFW_DIR})

#set CMP0072 explicity to use modern OpenGL(GLVND) implementation
cmake_policy(SET CMP0072 NEW)
set(OpenGL_GL_PREFERENCE "GLVND")

# Find the OpenGL package
find_package(OpenGL REQUIRED)

# Include directories for GLAD
target_include_directories(project PRIVATE glad/)

# Link the GLFW and OpenGL libraries to the executable
target_link_libraries(project PRIVATE glfw OpenGL::GL)
