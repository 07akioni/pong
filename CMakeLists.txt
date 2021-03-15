cmake_minimum_required(VERSION 3.18)

project(Pong)

if (EMSCRIPTEN)
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -s USE_GLFW=3 -s ASSERTIONS=1 -s WASM=1 -s ASYNCIFY")
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -s USE_GLFW=3 -s ASSERTIONS=1 -s WASM=1 -s ASYNCIFY")
    set(CMAKE_EXECUTABLE_SUFFIX ".html")
endif ()

# find_library(cocoa_lib Cocoa)
# find_library(opengl_lib OpenGL)
# find_library(iokit_lib IOKit)

add_subdirectory(Pong)
