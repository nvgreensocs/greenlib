# enabling SystemC2.1 automatically changes 
# includes and compiler flags in Makefile.defs
#SYSTEMC21V1 = yes

ifneq ($(strip $(GSROOT)),)
  # Using GSPM, load more dependencies in Makefile.gspm
  BUILD_DEPENDS = scv
endif

CC     = g++
#OPT    = -O3 -funroll-loops -mtune=pentium4
OPT  = -g -Wall -lpthread -D_REENTRANT
#OTHER  = -Wno-deprecated
CFLAGS = $(OPT) $(OTHER)
# CFLAGS = $(DEBUG) $(OTHER)
EXTRA_LIBS = -lscv #-lboost_program_options

MODULE = testbench_demonstration_platform
SRCS = testbench_demonstration_platform.cpp Mem.cpp ddr_ram.cpp TG.cpp Cache.cpp PCIeDevice.cpp lru_cache.cpp
# scml_property.cpp
#./gscontrol/scml/scml_property.cpp
OBJS = $(SRCS:.cpp=.o)
#OBJS =
#scml_property.o
#scml_property.o

include ../Makefile.gspm
include ../Makefile.defs

all: $(EXE)

