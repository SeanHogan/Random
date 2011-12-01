all: pgzip

debug:		gzip.c bits.c deflate.c util.c trees.c threads.c
		gcc -O3 -lpthread gzip.c bits.c deflate.c util.c trees.c threads.c zip.c -o debug_pgzip

pgzip:		gzip.o zip.o deflate.o trees.o bits.o util.o threads.o
		gcc -O3 -lpthread gzip.o zip.o deflate.o trees.o bits.o util.o threads.o -o pgzip

gzip.o:		gzip.c
		gcc -O3 -c gzip.c

zip.o:		zip.c
		gcc -O3 -c zip.c

deflate.o:	deflate.c
		gcc -O3 -c deflate.c

trees.o:	trees.c
		gcc -O3 -c trees.c

bits.o:		bits.c
		gcc -O3 -c bits.c

util.o:		util.c
		gcc -O3 -c util.c

threads.o:	threads.c
		gcc -O3 -c threads.c 

clean:		
		rm *.o
