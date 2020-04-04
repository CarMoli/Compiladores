grammar.tab.c: grammar.y
	bison -d grammar.y
lex.yy.c: grammar.l grammar.tab.c
	flex grammar.l
grammar.tab.o: grammar.tab.c
	gcc grammar.tab.c -c
lex.yy.o: lex.yy.c
	gcc lex.yy.c -c

a.out: grammar.tab.o lex.yy.o
	gcc grammar.tab.o lex.yy.o -lfl
run: a.out
	./a.out
clean:
	rm -r a.out *.c *.o *.h
