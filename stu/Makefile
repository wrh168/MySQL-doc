CC=gcc
AFLAGS=-Wall -g
LDFLAGS= -lmysqlclient
OBJS= add.cgi del.cgi mod.cgi sel.cgi add_school.cgi sel_school.cgi	mod_school.cgi del_school.cgi add_course.cgi	sel_course.cgi	mod_course.cgi	del_course.cgi

all:$(OBJS)

$(OBJS):%.cgi:%.c
	$(CC) $(AFLAGS) $< cgic.c -o $@ $(LDFLAGS)

.PHONY:clean
clean:
	rm ./*.cgi
install:
	cp *.cgi /usr/lib/cgi-bin/sx
	cp head.html footer.html index.html /usr/lib/cgi-bin/sx/
