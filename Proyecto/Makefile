a.out: main.o lex.yy.o bison.tab.o
		gcc main.o lex.yy.o bison.tab.o -ll

main.o: main.c bison.tab.c
		gcc -c main.c

lex.yy.o: lex.yy.c
		gcc -c lex.yy.c

bison.tab.o: bison.tab.c
		gcc -c bison.tab.c 

lex.yy.c: flex.l bison.tab.c
		flex flex.l

bison.tab.c: bison.y
		bison -d bison.y

clean:
		rm -f a.out main.o lex.yy.o bison.tab.o lex.yy.c bison.tab.c bison.tab.h

run: a.out
		./a.out
