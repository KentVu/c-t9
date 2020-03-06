cmake_minimum_required(VERSION 3.6)
project(c_t9)

set(CMAKE_CXX_STANDARD 14)

include_directories(include)
#include_directories(include/t9)
include_directories(libraries)
#include_directories(libraries/kvec)
#include_directories(libraries/list)
# meson-Generated
include_directories(build/include)

add_executable(c_t9
        libraries/list/iterator.c
        libraries/list/list.c
        libraries/list/list_node.c
        src/t9/corpus.c
        src/t9/io.c
        src/t9/math.c
        src/t9/model.c
        src/t9/node.c
        src/t9/path.c
        src/t9/timer.c
        src/t9/tree.c
        src/main.c)


#find_library( # Defines the name of the path variable that stores the
#              # location of the NDK library.
#              log-lib
#
#              # Specifies the name of the NDK library that
#              # CMake needs to locate.
#              log )

# Links your native library against one or more other native libraries.
#target_link_libraries( # Specifies the target library.
#                       dawgdic-build
#
#                       # Links the log library to the target library.
#                       ${log-lib} )
