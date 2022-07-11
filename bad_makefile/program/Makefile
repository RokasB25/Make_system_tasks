CFLAGS:=-I./ -Wall -Ipwd
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)
BIN:=calculator

all: $(BIN)

$(BIN):$(OBJS)
	$(CC) -o $@ $^
	
clean:
	$(RM) $(BIN) $(OBJS)
