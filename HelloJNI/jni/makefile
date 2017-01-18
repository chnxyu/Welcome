
# Define a variable for classpath
CLASS_PATH = ../bin

# Define a virtual path for .class in the bin directory
vpath %.class $(CLASS_PATH)

all : libhello.so

# $@ matches the target, $< matches the first dependancy
libhello.so : HelloJNI.o
	gcc -o libhello.so -shared HelloJNI.o

# $@ matches the target, $< matches the first dependancy
HelloJNI.o : HelloJNI.c HelloJNI.h
	gcc -fpic -I/usr/lib/jvm/java-8-oracle/include -I/usr/lib/jvm/java-8-oracle/include/linux -c HelloJNI.c -o $@
# $* matches the target filename without the extension
HelloJNI.h : HelloJNI.class
	javah -classpath $(CLASS_PATH) $*

clean :
	rm HelloJNI.h HelloJNI.o libhello.so