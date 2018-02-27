CFLAGS=-g3
LDFLAGS=-pthread

.PHONY: clean all

all: myapp

functions.o: functions.c functions.h
	$(CC) $(CFLAGS) -c functions.c

main.o: main.c main.h functions.h
	$(CC) $(CFLAGS) -c main.c

myapp: main.o functions.o
	$(CC) $(LDFLAGS) main.o functions.o -o myapp

clean:
	rm -f *.o *~ myapp
