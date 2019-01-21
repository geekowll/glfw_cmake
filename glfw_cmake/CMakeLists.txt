# CMakeList.txt : CMake project for glfw_cmake, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

add_definitions(-DGLEW_STATIC)

include_directories("include" "D:/GLFW/include")
link_directories("D:/GLFW/lib" )

file(GLOB SRC_LIST source/*.cpp source/GL/*.c)
# Add source to this project's executable.
add_executable (glfw_cmake ${SRC_LIST})

# TODO: Add tests and install targets if needed.
target_link_libraries(glfw_cmake glfw3.lib opengl32.lib glu32.lib )