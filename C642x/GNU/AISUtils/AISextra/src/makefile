#############################################################
# Makefile for TI AISExtra project.                         #
#   Generates the COFF AISExtra file which is used to       #
#   supplement the AIS ROM bootloader to add the ability    #
#	  to boot successfully over UART and to change the power  #
#	  domain states of the device's Local Power Domains.      #
#############################################################
# Auth: Daniel Allred
#
PROGRAM:=AISExtra
DEVSTRING:=C642x

CROSSCOMPILE=
CC=$(CROSSCOMPILE)cl6x
SOURCES=$(PROGRAM).c

CFLAGS=-O=2 -c -I=../../../../../Common/include -I=../../../../Common/include -I=../../../Common/include -I=../include -ms3 -mv6400+ --symdebug:none
LNKFLAGS=-z -a -e_LPSCTransition -w -x

OBJECTS:=$(patsubst %.c,%.obj,$(SOURCES))
EXECUTABLE:=../$(PROGRAM)_$(DEVSTRING).out
LINKERSCRIPT=$(PROGRAM).cmd

all: $(EXECUTABLE) $(OBJECTS)

.PHONY : clean objclean
clean:
		-rm -f -v $(OBJECTS) $(EXECUTABLE)
		
objclean:
		-rm -f -v $(OBJECTS)

$(EXECUTABLE): $(OBJECTS)
		$(CC) $(LNKFLAGS) -o=$@ $(LINKERSCRIPT) $(OBJECTS)
		
%.obj : %.c %.h
		$(CC) $(CFLAGS) $< 

vpath %.h ../../../../Common/include:../../../Common/include:../../Common/include:../include        

