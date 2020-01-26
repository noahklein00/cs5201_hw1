###############################################################################
## -->Makefile<--
###############################################################################
##
## Programmer : Noah Klein
## Instructor : Price
## Class      : CS5201 Spring 2020
## Assignment : Homework 1 - Makefiles
## Filename   : Makefile
##
###############################################################################

###############################################################################
## This makefile will build an executable for the ex1 directory.
###############################################################################

default: all

all: driver

driver: additives.o\
		beer.o\
		brewMain.o
	g++ additives.o beer.o brewMain.o -o driver

clean:
	-@rm -f core > /dev/null 2>&1
	-@rm -f driver > /dev/null 2>&1
	-@rm -f additives.o beer.o brewMain.o > /dev/null 2>&1

# Dependency lists for the various source files
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