cmake_minimum_required(VERSION 3.24)
project(OpenGL_Full)

set(CMAKE_CXX_STANDARD 14)

# Include .cpp files here
set(SOURCE_FILES OpenGL_Full/main.cpp OpenGL_Full/glad.c)

# Include .h files here
set(HEADER_FILES)

# Include the .cpp and .h files as executables
add_executable(OpenGL_Full ${SOURCE_FILES} ${HEADER_FILES})

# Include directories
include_directories(OpenGL_Full Linking/include)
include_directories(GLAD/include)

# include subdirectory
add_subdirectory(dependencies)

# Link libraries
target_link_libraries(OpenGL_Full glfw)

