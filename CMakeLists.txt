cmake_minimum_required(VERSION 2.8)
project(nwn-tools)

#find_program(bison bison)
#if (NOT bison)
#	message(FATAL_ERROR "Cannot find bison, need bison installed to generate Parser/Lexer")
#endif (NOT bison)

find_package(BISON)
if (NOT BISON_FOUND)
	message(FATAL_ERROR "Cannot find bison, need bison installed to generate Parser/Lexer")
endif (NOT BISON_FOUND)

#set(CMAKE_CXX_FLAGS "-Wall -Wno-unused -Wno-write-strings -Wno-deprecated")
#set(CMAKE_CXX_FLAGS " -w -O2 -m32")
set(CMAKE_CXX_FLAGS "-g -w -m32")

if (BISON_VERSION VERSION_GREATER "3.0.0")
   add_definitions(-DNWN_BISON_3=1)
endif (BISON_VERSION VERSION_GREATER "3.0.0")

add_subdirectory(_MathLib)
add_subdirectory(_NmcLib)
add_subdirectory(_NwnLib)
add_subdirectory(_NscLib)
add_subdirectory(nwnnsscomp)
add_subdirectory(nwnmdlcomp)
