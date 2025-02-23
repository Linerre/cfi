CC = javac
JAVA = java
OPS = -d .
srcfile = GenerateAst.java
CLASSPATH = craftinginterpreters.tool

run: build
	$(JAVA) -cp ./ $(CLASSPATH).GenerateAst ./

build: GenerateAst.java
	$(CC) $(OPS) $<
