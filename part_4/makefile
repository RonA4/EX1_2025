CC = gcc
CFLAGS = -Wall 

all: main advmath.so

main: main.o advmath.so
	$(CC) $(CFLAGS) -o main main.o ./advmath.so

main.o: main.c
	$(CC) $(CFLAGS) -c main.c

advmath.so: advmath.o
	$(CC) -shared -o advmath.so advmath.o

advmath.o: advmath.c advmath.h
	$(CC) -fPIC $(CFLAGS) -c advmath.c

clean:
	rm -f main main.o advmath.so advmath.o