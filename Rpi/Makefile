#############################################################################

# The recommended compiler flags for the Raspberry Pi
CCFLAGS=-Wall -mfpu=vfp -mfloat-abi=hard -march=armv6zk -mtune=arm1176jzf-s -ldispatch -lBlocksRuntime -fblocks -L../RF24/librf24-rpi/librf24  -lrf24 -I../RF24Network/ -I../RF24/librf24-rpi/librf24
#CCFLAGS=

# define all programs
PROGRAMS = rpihub 
SOURCES = ${PROGRAMS:=.cpp} ../RF24Network/RF24Network.cpp ../RF24Network/Sync.cpp

all: ${PROGRAMS}

${PROGRAMS}: ${SOURCES}
#	g++ ${CCFLAGS} -Wall $@.cpp -o $@
	clang ${CCFLAGS}  ${SOURCES} -o $@

clean:
	rm -rf $(PROGRAMS)

