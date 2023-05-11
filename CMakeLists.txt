cmake_minimum_required(VERSION 3.10)
project(first_example)

add_subdirectory(dependencies)

add_executable(first_example src/example.cpp)

if(MSVC)
    set(CMAKE_EXE_LINKER_FLAGS /MANIFEST:NO)
endif()

target_link_libraries(first_example xtensor)
