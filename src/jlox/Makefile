CC := javac
JAVA := java
BUILD := ./build
OPS := -d ./$(BUILD)
lexer := ./lox/*.java
CLASSPATH := craftinginterpreters.lox

build:
	$(CC) $(OPS) $(lexer)

print:
	$(JAVA) -cp $(BUILD) $(CLASSPATH).AstPrinter
