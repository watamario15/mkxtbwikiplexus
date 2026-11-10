CC=gcc
CXX=g++
LD=g++

XML2_PREFIX?=/usr
LD_PREFIX?=/usr/local

CCFLAGS=-Wall -O3 -D_LARGEFILE_SOURCE=1 -D_LARGEFILE64_SOURCE=1 -D_FILE_OFFSET_BITS=64 -DNDEBUG -I$(XML2_PREFIX)/include/libxml2
CXXFLAGS=$(CCFLAGS)
LDFLAGS=-L$(LD_PREFIX)/lib

LDLIBS_WIKIPLEXUS=-Wl,-Bstatic -lxml2 $(filter-out -lxml2 -llzma -lz,$(XML_PC)) -llzma -lz -Wl,-Bdynamic
LDLIBS_INDEX=
LDLIBS_IMAGECOMPLEX=$(LDLIBS_WIKIPLEXUS)
LDLIBS_YOMI=-lmecab -lkakasi
LDLIBS_MKRAX=-Wl,-Bstatic -llzma -Wl,-Bdynamic

TARGETPOSTFIX=-bin
SRCDIR=..
include $(SRCDIR)/Makefile.i
