EXE=hello
OBJS=a.o b.o
CC=gcc
$(EXE): $(OBJS)
	$(CC) $^ -o $@
.c .o:
	$(CC) -c $<
clean:
	rm -rf *.o $(EXE)
