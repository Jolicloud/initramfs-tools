UDEV_CFLAGS = $(shell pkg-config --cflags libudev)
UDEV_LIBS = $(shell pkg-config --libs libudev)

CC = gcc
CFLAGS = -g -Wall -O2 $(UDEV_CFLAGS)
LDFLAGS =


.PHONY: all
all: wait-for-root

wait-for-root: wait-for-root.o
	$(CC) $(LDFLAGS) -o $@ $< $(UDEV_LIBS)

.PHONY: clean
clean:
	rm -f wait-for-root.o wait-for-root core *~
