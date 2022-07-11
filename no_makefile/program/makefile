BIN:=calculator
CPPFLAGS:=-I./ -Wall 
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)

.PHONY: all clean

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) -o $@ $^

%.o:%.c
	$(CC) $(CPPFLAGS) -c -o $@ $^

clean:
	$(RM) $(BIN) $(OBJS)