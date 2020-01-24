#Noah Klein
#cs5201
#Price
#Homework 1 - Makefiles

default: all
all: driver
driver: additives.o\
        beer.o\
        brewMain.o
	g++ additives.o beer.o brewMain.o -o driver

additives.o: additives.cpp\
			 additives.h
	g++ -c additives.cpp

beer.o: beer.cpp\
		beer.h\
		yeast.h\
		hops.h\
		grains.h
	g++ -c beer.cpp

brewMain.o: brewMain.cpp\
			wine.h\
			yeast.h\
			additives.h\
			wine.hpp\
			beer.h\
			hops.h\
			grains.h
	g++ -c brewMain.cpp