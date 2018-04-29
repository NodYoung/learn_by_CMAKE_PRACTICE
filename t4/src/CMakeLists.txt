FIND_PATH(myHeader hello.h)  # export CMAKE_INCLUDE_PATH=/home/ubuntu/cmake/tmp/t3/usr/include/hello
MESSAGE(STATUS "myHeader dir is:" ${myHeader})
IF(myHeader)
INCLUDE_DIRECTORIES(${myHeader})
ENDIF(myHeader)
# INCLUDE_DIRECTORIES(/home/ubuntu/cmake/tmp/t3/usr/include/hello)
# set include path of hello.h

LINK_DIRECTORIES(/home/ubuntu/cmake/tmp/t3/usr/lib) # LINK_DIRECTORIES must set before ADD_EXECUTABLE

ADD_EXECUTABLE(main main.c)

TARGET_LINK_LIBRARIES(main libhello.so)