LEX = flex
YACC = bison 
CC = gcc

install : y.tab.c y.tab.h
	$(CC) y.tab.c -o ZtoZ3
	
y.tab.c y.tab.h : ZtoZ3.y lex.yy.c
	$(YACC) -d ZtoZ3.y -o y.tab.c
	
lex.yy.c : ZtoZ3.l
	$(LEX) ZtoZ3.l

clean:
	rm -rf *.h
	rm -rf *.c
	
uninstall:
	rm -rf ZtoZ3
	rm -rf ZtoZ3.exe


