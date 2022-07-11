BIN:=main
CFLAGS:=-Wall
ASFLAGS:=-shared
CPPFLAGS:=-I./
LDFLAGS:=-fPIC
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)
LIB:=library.so

.PHONY: all clean

all: library $(BIN)

library:file_reader.o
	$(CC) $(ASFLAGS) -o $(LIB) $^
	
file_reader.o:file_reader.c
	$(CC) -c $(LDFLAGS) -o $@ $^

$(BIN): $(OBJS)
	$(CC) $(CPPFLAGS) $(CFLAGS) -o $@ $^ $(LIB)

%.o:%.c
	$(CC) -c -o $@ $^

clean:
	$(RM) $(OBJS) $(BIN) $(LIB)