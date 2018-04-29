PROJECT(HELLO)  
# define project name, define <projectname>_BINARY_DIR and <projectname>_SOURCE_DIR implicitly

SET(SRC_LIST main.c)   
# define variable explicitly

MESSAGE(STATUS "This is BINARY dir " ${HELLO_BINARY_DIR})
MESSAGE(STATUS "This is SOURCE dir " ${HELLO_SOURCE_DIR})
# output info to terminal

ADD_EXECUTABLE(hello ${SRC_LIST})
# generate executable file