src = $(wildcard ../src/*.c) $(wildcard ../src/sdl2/*.c) $(wildcard ../src/sdl_common/*.c) ../src/lib/ini/ini.c ../src/null/virtualKeyboard.c
obj = $(src:.c=.o)
CC = ppc-morphos-gcc
STRIP = ppc-morphos-strip
LDFLAGS = -lSDL2_mixer -noixemul -lSDL2 -L/usr/local/lib -lm

CFLAGS = -noixemul -I/usr/local/include -DHAVE_SDL2 -O2 -Wall

opensupaplex: $(obj)
	$(CC) -o $@ $^ $(LDFLAGS)
	$(STRIP) --strip-all $@
clean:
	rm $(obj)