cmake_minimum_required(VERSION 3.14)
project(OpenGLTest)

set(CMAKE_CXX_STANDARD 17)

add_executable(OpenGLTest main.cpp ShaderManager.cpp ShaderManager.h Actor.h Triangle.cpp Triangle.h)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(GLEW REQUIRED)
include_directories( ${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS} ${GLEW_INCLUDE_DIRS} )
target_link_libraries(OpenGLTest ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${GLEW_LIBRARY} )