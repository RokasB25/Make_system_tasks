CFLAGS:=-shared
LIB:=libcalculator.so
DESTDIR:=~/Documents
PREFIX:=Praktika
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)

.PHONY: all install uninstall clean

all: $(LIB) 

$(LIB):math_functions.o
	$(CC) $(CFLAGS) -o $@ $^

%.o:%.c
	$(CC) -c -fPIC -o $@ $^

install: $(LIB)
	install -d $(DESTDIR)/$(PREFIX)/include
	install -m 644 ./$(LIB) $(DESTDIR)/$(PREFIX)/include/$(LIB)

uninstall:
	$(RM) $(DESTDIR)/$(PREFIX)/include/$(LIB)

clean:
	$(RM) $(OBJS) $(LIB)
