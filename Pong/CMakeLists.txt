project(Pong LANGUAGES C)

aux_source_directory(./src DIR_SRCS)

include_directories(../libs/raylib/raylib/include)
link_directories(../libs/raylib/raylib)

add_executable(
    Pong
    ${DIR_SRCS}
)

# message(${cocoa_lib} " " ${opengl_lib} " " ${iokit_lib})
# /Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk/System/Library/Frameworks/Cocoa.framework /Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk/System/Library/Frameworks/OpenGL.framework/Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk/System/Library/Frameworks/IOKit.framework



# target_link_libraries(Pong PRIVATE ${cocoa_lib} ${opengl_lib} ${iokit_lib} libraylib.a)
# target_link_libraries(Pong PRIVATE /Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk/System/Library/Frameworks/Cocoa.framework /Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk/System/Library/Frameworks/OpenGL.framework /Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk/System/Library/Frameworks/IOKit.framework libraylib.a)
target_link_libraries(Pong PRIVATE libraylib.a)