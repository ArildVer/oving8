# program executable name
TARGET = out
# path to gcc
CC = /home/student/Desktop/test2/buildroot-avr32-v3.0.0_TTK4147/output/staging/usr/bin/avr32-linux-gcc
# compiler flags
CFLAGS = -g -Wall
# linker flags
LDFLAGS = -g -lrt
# list of sources
SOURCES = $(shell find -name "*.c")
# default rule, to compile everything
all: $(TARGET)
# define object files
OBJECTS = $(SOURCES:.c=.o)
# link programs
$(TARGET): $(OBJECTS)
	$(CC) $(LDFLAGS) -o $@ $^
# compile
%.o : %.c
	$(CC) $(CFLAGS) -c -o $@ $<
# cleaning
clean:
	rm -f $(TARGET) $(OBJECTS)
