CC := javac
JAVA := java
BUILD := ./build
OPS := -d ./$(BUILD)
CLASSPATH := craftinginterpreters.lox
SOURCE := ./lox/*.java

run:
	$(JAVA) -cp $(BUILD) $(CLASSPATH).Lox

build: $(SOURCE)
	$(CC) $(OPS) $(SOURCE)

print:
	$(JAVA) -cp $(BUILD) $(CLASSPATH).AstPrinter
