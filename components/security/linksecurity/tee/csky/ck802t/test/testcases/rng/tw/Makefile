#
# Copyright (C) 2015-2017 Alibaba Group Holding Limited
#

TOP := $(PWD)/../../../../src/tw
CURRENT_BUILD := TW
include $(TOP)/tee.cfg
include $(TOP)/Make.rules

CFLAGS  += -I../inc/ -I./

SRCS := $(wildcard *.c *.cxx)
OBJS := $(patsubst %.cxx,%.o,$(patsubst %.c,%.o,$(SRCS)))

.PHONY: all clean

all: built-in.o

built-in.o: $(OBJS)
	$(LD) -r $^ -o $@

clean:
	rm -f *.o built-in.*
