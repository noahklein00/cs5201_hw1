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
## This makefile will build an executable for the ex2 directory.
###############################################################################

CXX = /usr/bin/g++
FLAGS = -W -Wall -g -pedantic-errors
OBJECTS = driver.o\
		  parser.o\
		  scanner.o\
		  signal.o\
		  token.o\
		  tokenlist.o

.SUFFIXES: .cpp

.cpp.o: $<
	${CXX} -c ${FLAGS} $< -o $@

default: all

all: driver

driver: ${OBJECTS}
	${CXX} ${FLAGS} ${OBJECTS} -o $@

clean:
	-@rm -f core > /dev/null 2>&1
	-@rm -f driver > /dev/null 2>&1
	-@rm -f ${OBJECTS} > /dev/null 2>&1
	
# Dependency lists for the various source files
driver.o: driver.cpp\
          signal.h\
          parser.h\
          tokenlist.h\
          token.h\
          enTokens.h\
          Amatrix.h\
          Avector.h\
          scanner.h\
          enChar.h
	g++ -c driver.cpp
	
parser.o: parser.cpp\
		  parser.h\
		  tokenlist.h\
		  token.h\
		  enTokens.h\
		  Amatrix.h\
		  Avector.h\
		  signal.h
	g++ -c parser.cpp
	
scanner.o: scanner.cpp\
		   scanner.h\
		   enChar.h\
		   tokenlist.h\
		   token.h\
		   enTokens.h\
		   signal.h
	g++ -c scanner.cpp
	
signal.o: signal.cpp\
		  signal.h
	g++ -c signal.cpp
	
token.o: token.cpp\
		 token.h\
		 enTokens.h
	g++ -c token.cpp
	
tokenlist.o: tokenlist.cpp\
			 tokenlist.h\
			 token.h\
			 enTokens.h\
			 signal.h
	g++ -c tokenlist.cpp
















