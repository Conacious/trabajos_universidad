GCC = g++

SRC = src
OBJ = obj
BIN = bin

objetos = $(OBJ)/ejercicio_01.o $(OBJ)/ejercicio_04.o $(OBJ)/ejercicio_06.o $(OBJ)/ejercicio_07.o $(OBJ)/ejercicio_08.o $(OBJ)/ejercicio_09.o
ejecutables = $(BIN)/ejercicio_01 $(BIN)/ejercicio_04 $(BIN)/ejercicio_06 $(BIN)/ejercicio_07 $(BIN)/ejercicio_08 $(BIN)/ejercicio_09

todo: directorios $(objetos) $(ejecutables)

directorios: 
	mkdir -p $(SRC)
	mkdir -p $(OBJ)
	mkdir -p $(BIN)
	@echo "\nGenerando ejecutables de los ejercicios...\n"

$(objetos): $(OBJ)/%.o: $(SRC)/%.cpp
	$(GCC) -c $< -o $@

$(ejecutables): $(BIN)/%: $(OBJ)/%.o
	$(GCC) -o $@ $<

clean :
	@echo "\nBorrando ficheros de codigo objeto y ejecutables...\n"
	rm $(OBJ)/* $(BIN)/* 
