cmake_minimum_required(VERSION 3.23)
project(doom C)
set(CMAKE_C_STANDARD 17)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
add_executable(doom main.c)
include_directories(${GLUT_INCLUDE_DIRS} ${OPENGL_INCLUDE_DIRS} )

target_link_libraries(doom ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} )
