CFLAGS = -Wall -pedantic -Werror
LFLAGS = `sdl-config --libs` -lSDL -lSDL_image -lSDL_mixer -lSDL_ttf
OBJS   = audio.o bullet.o collisions.o draw.o entity.o font.o init.o input.o graphics.o main.o player.o ufo.o
PROG = tutorial07
CXX = gcc

# top-level rule to create the program.
all: $(PROG)

# compiling other source files.
%.o: src/%.c src/%.h src/defs.h src/structs.h
	$(CXX) $(CFLAGS) -c -s $<

# linking the program.
$(PROG): $(OBJS)
	$(CXX) $(OBJS) -o $(PROG) $(LFLAGS)

# cleaning everything that can be automatically recreated with "make".
clean:
	rm $(PROG) *.o
