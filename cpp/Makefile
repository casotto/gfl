CC=c++
NVCC=nvcc
CFLAGS=-O3 -Wall -Wextra -ansi -std=c99 -pedantic -I"C:\projects\gsl\include" -L"C:\projects\gsl\lib" -lgslcblas -lgsl -lm
OBJ=obj/*.o
IDIR=../include/

all:
	mkdir -p lib
	mkdir -p obj
	cd obj; ${CC} ${CFLAGS}  -c -fPIC ../src/*.c -I${IDIR}
	${CC} -shared -o lib/libgraphfl.so ${OBJ} -lgsl -lgslcblas
	
docs:
	doxygen Doxyfile

clean:
	rm obj/*.o

cleanall:
	rm obj/*.o
	rm lib/*.so
