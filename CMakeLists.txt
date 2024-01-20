cmake_minimum_required(VERSION 3.7)

project(sandy)

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})

add_executable(sandy main.cc)
target_link_libraries(sandy ${SDL2_LIBRARIES})
set_target_properties(sandy PROPERTIES
	CXX_STANDARD 17
	CXX_STANDARD_REQUIRED YES
	CXX_EXTENSIONS NO
)