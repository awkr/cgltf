cmake_minimum_required(VERSION 3.26)
project(cgltf)

set(CMAKE_CXX_STANDARD 17)

add_library(cgltf STATIC cgltf.h cgltf_write.h cgltf.c)
target_include_directories(cgltf PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_definitions(cgltf PRIVATE $<$<CONFIG:Debug>:CGLTF_VALIDATE_ENABLE_ASSERTS=1>)
