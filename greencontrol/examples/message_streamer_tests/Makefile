# enabling SystemC2.1 automatically changes 
# includes and compiler flags in Makefile.defs
#SYSTEMC21V1 = yes

CC     = g++
#OPT    = -O3 -funroll-loops -mtune=pentium4
OPT  = -g -Wall -lpthread -D_REENTRANT
#OTHER  = -Wno-deprecated
CFLAGS = $(OPT) $(OTHER) -DSC_INCLUDE_DYNAMIC_PROCESSES
# CFLAGS = $(DEBUG) $(OTHER) -DSC_INCLUDE_DYNAMIC_PROCESSES
EXTRA_LIBS = -lscv # -lboost_program_options

MODULE = testbench_message_streamer_tests
SRCS = testbench_message_streamer_tests.cpp
OBJS = $(SRCS:.cpp=.o)

include ../Makefile.gspm
include ../Makefile.defs

all: $(EXE)
