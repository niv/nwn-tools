cmake_minimum_required(VERSION 2.8)
project(nwn-tools)

#set(CMAKE_CXX_FLAGS "-Wall -Wno-unused -Wno-write-strings -Wno-deprecated")
set(CMAKE_CXX_FLAGS "-w")

add_subdirectory(_MathLib)
add_subdirectory(_NmcLib)
add_subdirectory(_NwnLib)
add_subdirectory(_NscLib)
add_subdirectory(nwnnsscomp)
add_subdirectory(nwnmdlcomp)
