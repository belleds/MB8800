# Generated automatically from Makefile.in by configure.
INSTALL = /usr/bin/install -c
INSTALL_PROGRAM = ${INSTALL}
INSTALL_DATA = ${INSTALL} -m 644

prefix = /usr/local
exec_prefix = ${prefix}

SHAREDOPT = -shared
LIBDIR = $(prefix)/lib
INCDIR = $(prefix)/include
MANDIR	= $(prefix)/man/man3
SHELL = /bin/sh
EXTRA_LIBS = 

INCS =  -Isrc
FLAGS = -Wall -fPIC

OBJS = src/error.o src/cgi.o src/session.o src/base64.o src/md5.o \
	src/string.o src/general.o src/list.o src/cookie.o

.c.o: 
	$(CC) $(FLAGS) -c $< -o $@

all: $(OBJS) src/libcgi.so

	@echo ""
	@echo ""
	@echo ""
	@echo "+---------------------------------------+"
	@echo "|       Thanks for using LibCGI         |"
	@echo "+---------------------------------------+"
	@echo "| LibCGI is getting better because      |"
	@echo "| people like you are using it. So, if  |"
	@echo "| LibCGI is helping you in some way,    |"
	@echo "| please help us to improve it, sending |"
	@echo "| suggestions, bug reports, bug fixes,  |"
	@echo "| and specially improvment code.        |"
	@echo "| You can subscribe to the mailing list |"
	@echo "| or send a mail to the author.         |"
	@echo "+---------------------------------------+---------------------------+"
	@echo "| List: http://lists.sourceforge.net/lists/listinfo/libcgi-general  |"
	@echo "+-------------------------------------------------------------------+"
	@echo ""


shared: src/libcgi.so
	cp src/libcgi.so $(LIBDIR)

src/libcgi.a: $(OBJS)
	$(AR) rc src/libcgi.a $(OBJS)

src/libcgi.so: src/libcgi.a
	$(CC) $(SHAREDOPT) -o src/libcgi.so $(OBJS) $(EXTRA_LIBS)

install:
	cp src/libcgi.a $(LIBDIR)
	cp src/libcgi.so $(LIBDIR)
	cp src/cgi.h $(INCDIR)
	cp src/session.h $(INCDIR)


src/error.o: src/error.c src/error.h
	$(CC) $(FLAGS) -c $< -o $@
src/cgi.o: src/cgi.c src/cgi.h
	$(CC) $(FLAGS) -c $< -o $@
src/session.o: src/session.c src/session.h
	$(CC) $(FLAGS) -c $< -o $@
src/base64.o: src/base64.c
	$(CC) $(FLAGS) -c $< -o $@
src/md5.o: src/md5.c
	$(CC) $(FLAGS) -c $< -o $@
src/string.o: src/string.c
	$(CC) $(FLAGS) -c $< -o $@
src/cookie.o: src/cookie.c
	$(CC) $(FLAGS) -c $< -o $@
src/general.o: src/general.c
	$(CC) $(FLAGS) -c $< -o $@
src/list.o: src/list.c
	$(CC) $(FLAGS) -c $< -o $@

clean:
	find src/ -name "*.*o" -exec rm -f {} \;
	find src/ -name "*.a" -exec rm -f {} \;

uninstall: clean
	rm -f $(LIBDIR)/libcgi.*
	rm -f $(INCDIR)/cgi.h
	rm -f $(INCDIR)/session.h
	rm -f $(MANDIR)/libcgi*

install_man:
	cp doc/man/man3/libcgi_base64.3 $(MANDIR)
	cp doc/man/man3/libcgi_cgi.3 $(MANDIR)
	cp doc/man/man3/libcgi_general.3 $(MANDIR)
	cp doc/man/man3/libcgi_string.3 $(MANDIR)
	cp doc/man/man3/libcgi_session.3 $(MANDIR)
	cp doc/man/man3/libcgi_cookie.3 $(MANDIR)

