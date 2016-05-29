SOURCE=json_reader.cpp json_value.cpp json_writer.cpp
LIBS=../../../src/DeviceManager/lib/`uname -s`
OUT=json_reader.o json_value.o json_writer.o
CPPFLAGS=-I ../../include
LIB=libjsoncpp.dylib
PREFIX=/usr/local/lib
${LIB}: ${OUT}
	@echo checking for ${LIBS} directory
	@mkdir -p ${LIBS}
	ld -arch x86_64 -dylib -lc -lc++ -o $@ ${OUT}

install: ${LIB}
	@echo cp ${LIB} ${PREFIX}
	@cp ${LIB} ${PREFIX}

devinstall: ${LIB}
	@echo cp ${LIB} ${LIBS}
	@cp ${LIB} ${LIBS}

clean:
	rm -f *.o ${LIB}
