#
# Makefile f�r NEO/Node, GNU GCC (g++)
#
# Filkataloger d�r andra delar av programet finns.
EDGE = ../Edge
NETWORK = ../Network
SET = ../Set
NODE = ../Node

# Kompilator
#CCC = g++
CC = g++

# Kompilatorflaggor, l�gg till '-g' om kompilering f�r avlusning ska g�ras.
CCFLAGS += -std=c++11 -pedantic -Wall -Wextra

# Preprocessorflaggor, -I l�gger till en filkatalog i inkluderingss�kv�gen.
CPPFLAGS += -I. -I.. -I$(NODE) -I$(SET) -I$(EDGE)

# L�nkflaggor - Fix f�r att l�sa lokala (IDA) problem med C++ l�nkbibliotek.
LDFLAGS += -L/sw/gcc-$(GCC4_V)/lib -static-libstdc++

Node.o: Node.h Node.cc $(EDGE)/Edge.h $(SET)/Set.h
	$(CC) $(CPPFLAGS) $(CCFLAGS) -c Node.cc

# 'make clean' tar bort objektkodsfiler och 'core' (minnesdump).
clean:
	@ \rm -rf *.o core

# 'make zap' tar �ven bort det k�rbara programmet och reservkopior (filer
# som slutar med tecknet '~').
#zap: clean
#	@ \rm -rf <programnamn> *~

# Se upp vid eventuell �ndring, '*' f�r absolut inte finnas f�r sig!!!
#
# '@' medf�r att kommandot inte skrivs ut p� sk�rmen d� det utf�rs av make.
# 'rm' �r ett alias f�r 'rm -i' p� IDA:s system, '\rm' inneb�r att "original-
# versionen", utan flaggan '-i', anv�nds. 
