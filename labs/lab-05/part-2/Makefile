all: dynamic_block static_block

static_block: program.o staticlibblock.a
	gcc program.o staticlibblock.a -o static_block

dynamic_block: program.o sharedlibblock.so
	gcc program.o sharedlibblock.so -o dynamic_block

staticlibblock.a: block.o
	ar qc staticlibblock.a block.o

sharedlibblock.so: block.o
	gcc -shared -o sharedlibblock.so block.o

block.o:
	gcc -fPIC -c source/block.c -o block.o

program.o:
	gcc -c program.c -o program.o

clean:
	rm static_block dynamic_block staticlibblock.a sharedlibblock.so block.o program.o
