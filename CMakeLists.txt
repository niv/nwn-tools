cmake_minimum_required(VERSION 2.8)
project(nwn-tools)

find_program(bison bison)
if (NOT bison)
	message(FATAL_ERROR "Cannot find bison, need bison installed to generate Parser/Lexer")
endif (NOT bison)


#set(CMAKE_CXX_FLAGS "-Wall -Wno-unused -Wno-write-strings -Wno-deprecated")
set(CMAKE_CXX_FLAGS "-w -O2")

add_subdirectory(_MathLib)
add_subdirectory(_NmcLib)
add_subdirectory(_NwnLib)
add_subdirectory(_NscLib)
add_subdirectory(nwnnsscomp)
add_subdirectory(nwnmdlcomp)
