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
	OUTPUT NscParser.cpp
	DEPENDS NscParser.ypp
	COMMAND yacc -S lalr1.cc NscParser.ypp -o NscParser.cpp
)
