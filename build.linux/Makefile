CC=gcc
CXX=g++
LD=g++
XML2_CFLAGS?= -I/usr/include/libxml2
XML2_LDFLAGS?= -L/usr/local/lib -lxml2 -llzma -lz

CXXFLAGS+= -O3 -D_LARGEFILE_SOURCE=1 -D_LARGEFILE64_SOURCE=1 -D_FILE_OFFSET_BITS=64 -DNDEBUG $(XML2_CFLAGS)
LDLIBS_WIKIPLEXUS+= -Wl,-Bstatic $(XML2_LDFLAGS) -Wl,-Bdynamic
LDLIBS_INDEX+=
LDLIBS_IMAGECOMPLEX+= $(LDLIBS_WIKIPLEXUS)
LDLIBS_YOMI+= -lmecab -lkakasi
LDLIBS_MKRAX+= -Wl,-Bstatic -llzma -Wl,-Bdynamic

TARGETPOSTFIX?=-bin
SRCDIR=..
include $(SRCDIR)/Makefile.i
