CFLAGS=-g3
LDFLAGS=-pthread
CC=gcc
ARMFLAGS = -m32 -arm -opt
ARMCC=arm-none-linux-gnueabi-$(CC)
MIPSFLAGS=${ARMFLAGS:arm=mips}

.PHONY: clean all

all: myapp

functions.o: functions.c functions.h
	$(ARMCC) $(CFLAGS) -c functions.c

main.o: main.c main.h functions.h
	$(ARMCC) $(CFLAGS) -c main.c

myapp: main.o functions.o
	$(ARMCC) $(MIPSFLAGS) $(LDFLAGS) main.o functions.o -o myapp

clean:
	rm -f *.o *~ myapp
	

