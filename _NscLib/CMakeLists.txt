add_library(nsc
	Nsc
	NscCodeGenerator
	NscCompiler
	NscContext
	NscDecompiler
	NscParserRoutines
	NscPStackEntry
	NscParser
)

add_custom_command(
	OUTPUT NscParser.cpp NscParser.hpp
	DEPENDS NscParser.ypp
	COMMAND ${BISON_EXECUTABLE} -S lalr1.cc NscParser.ypp -o NscParser.cpp
)
