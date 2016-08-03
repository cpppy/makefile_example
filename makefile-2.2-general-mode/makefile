#************************************************

# Copyright        :  

#

# Author           :   ene

# Date             :   2016-08-01

# Version          :   learn-1

# Description  :   Demo

#

#***********************************************/



SHELL = /bin/sh

LIB_DIR = /home/ene/leetcode/mfln/lib/
BIN_DIR = /home/ene/leetcode/mfln/bin/
OBJ_DIR = /home/ene/leetcode/mfln/test/obj/
SRC_DIR = /home/ene/leetcode/mfln/src/

$(shell mkdir -p ${LIB_DIR})
$(shell mkdir -p ${BIN_DIR})
$(shell mkdir -p ${OBJ_DIR})

RM = rm -fr

#************************************************

CC = g++
AR = ar rc

SRC_OBJECT = $(SRC_DIR)test_a.cc $(SRC_DIR)test_b.cc $(SRC_DIR)test_c.cc
H_OBJECT = $(SRC_DIR)so_test.h
OBJECT = test_a.o test_b.o test_c.o

MFLN_SRC_OBJECT = $(SRC_DIR)testabc.cc
MFLN_OBJECT = testabc.o

LIB_OBJECT = libtest.a
BIN_OBJECT = testabc

#************************************************

.PHONY:all
all:$(LIB_OBJECT) $(BIN_OBJECT)

$(LIB_OBJECT):$(OBJECT)
	$(AR) $(LIB_OBJECT) $(OBJECT)
	mv $(LIB_OBJECT) $(LIB_DIR)
	
	
$(OBJECT):$(SRC_OBJECT) $(H_OBJECT)
	$(CC) -c $(SRC_OBJECT)

$(BIN_OBJECT):$(MFLN_OBJECT)
	$(CC) -o $(BIN_OBJECT) $(OBJECT_DIR)$(MFLN_OBJECT) $(LIB_DIR)$(LIB_OBJECT)
	mv $(BIN_OBJECT) $(BIN_DIR)

$(MFLN_OBJECT):$(MFLN_SRC_OBJECT)
	$(CC) -c $(MFLN_SRC_OBJECT) -o $(MFLN_OBJECT)
	mv $(OBJECT)  $(OBJECT_DIR)
	mv $(MFLN_OBJECT) $(OBJECT_DIR)

clean:
	$(RM) $(LIB_DIR) $(BIN_DIR) $(OBJECT_DIR)

 
