# Build environment can be configured the following
# environment variables:
#   CC : Specify the C compiler to use
#   CFLAGS : Specify compiler options to use
#
#

CFLAGS += -I. -I../../lib/lib330 -I../../lib/libmseed -I../../libdali -DPACKAGE_VERSION=\"1.3.1\"
LIBS = ../../lib/lib330/lib330.a ../../lib/libmseed/libmseed.a ../../lib/libdali/libdali.a -lpthread -lrt -lm -lc

all: quant2dali

quant2dali: quant2dali.o dsarchive.h dsarchive.o ping.h ping.o 
	$(CC) $(CFLAGS) -o $@ quant2dali.o dsarchive.o ping.o $(LIBS)

clean:
	rm -f quant2dali.o quant2dali dsarchive.o ping.o

# Implicit rule for building object files
%.o: %.c
	$(CC) $(CFLAGS) -c $<

install:
	@echo
	@echo "No install target, copy the executable(s) yourself"
	@echo
