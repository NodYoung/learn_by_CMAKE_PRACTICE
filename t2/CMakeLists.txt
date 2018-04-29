PROJECT(HELLO)  
# define project name, define <projectname>_BINARY_DIR and <projectname>_SOURCE_DIR implicitly

ADD_SUBDIRECTORY(src bin)
# add source_dir, and binary_dir

INSTALL(FILES COPYRIGHT README DESTINATION share/doc/cmake/t2)
# install README/COPYRIGHT
INSTALL(PROGRAMS runhello.sh DESTINATION bin)
# install runhello.sh
INSTALL(DIRECTORY doc/ DESTINATION share/doc/cmake/t2)
# install doc/hello.txt
