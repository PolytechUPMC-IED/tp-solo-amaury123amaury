# definitions des variables
ID3= /home/sasl/shared/main3/env/tools
CC= g++
CFLAGS= -Wall
LDLIBS= -lid3 -lz
CPPFLAGS= -I/home/sasl/shared/main3/env/tools/include
CLIBS= -L/home/sasl/shared/main3/env/tools/lib

#all
all: %.o
			$(CC) $^ -o id3v2 $(CFLAGS)
			 
%.o: %.cpp
			$(CC) $(CPPFLAGS)
			-DVERSION="\"${VERSION}\"" -c -o %.o %.cpp
			
id3v2: convert.o list.o id3v2. genre.o libd3
			$(CC) $(CLIBS) $(CFLAGS) -o id3v2
			covert.o list.o id3v2.o genre.o $(LDLIBS)
			
#supprime les fichiers temporaires
clean:
			rm -rf *.o  
			
.PHONY: all clean
			
#question 8: Pour modifier LD_LIBRARY_PATH on tape:
#LD_LIBRARY_PATH=/home/sasl/shared/main3/env/tools/lib:$(LD_LIBRARY_PATH)
#export LD_LIBRARY_PATH

#question 9: Il faut utiliser une variable d'environnement contenant l'adresse absolu de id3v2

			

			
