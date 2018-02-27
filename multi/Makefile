CC = gcc
CFLAGS = -g3
LDFLAGS = -static

all: app1 app2 app3 

app1: app1.o common.o
app2: app2.o common.o
app3: app3.o common.o tools.o



install: app1 app2 app3
	cp -v app1 app2 app3 ./install
	
clean:
	rm -v app1 app2 app3 *.o
