CFLAGS:=-c -Wall -Weffc++ -g -std=c++11 -Iinclude
LFLAGS  = -L/usr/lib -lboost_system -lboost_thread -lboost_locale

all: BBclient
	g++ -o bin/BBclient bin/connectionHandler.o bin/BBclient.o $(LFLAGS)

BBclient: bin/connectionHandler.o bin/BBclient.o 
	
bin/connectionHandler.o: src/connectionHandler.cpp
	g++ $(CFLAGS) -o bin/connectionHandler.o src/connectionHandler.cpp

bin/BBclient.o: src/BBclient.cpp
	g++ $(CFLAGS) -o bin/BBclient.o src/BBclient.cpp
	
	
.PHONY: clean
clean:
	rm -f bin/*
