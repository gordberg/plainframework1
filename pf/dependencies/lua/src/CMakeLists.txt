INCLUDE_DIRECTORIES(baselib)

SET(TF_CURRENT_BINARY_PATH_LIB "../../dll")
SET(SRC_LIST lvm.h
             ldebug.h
             lmem.c
             lobject.c
             lparser.h
             lstate.h
             lstring.h
             lobject.h
             loadlib.c
             lfunc.h
             lundump.h
             lopcodes.c
             llimits.h
             lopcodes.h
             ltable.h
             lstring.c
             lbitlib.c
             lbaselib.c
             lua.c
             ldump.c
             lvm.c
             liolib.c
             lapi.c
             lcode.h
             ltm.h
             lctype.h
             lauxlib.h
             lctype.c
             lzio.c
             ldebug.c
             lparser.c
             linit.c
             ltm.c
             ltable.c
             llex.h
             lundump.c
             loslib.c
             ltablib.c
             lfunc.c
             lcode.c
             llex.c
             lcorolib.c
             luaconf.h
             lgc.c
             lmathlib.c
             ldo.h
             lstrlib.c
             ldo.c
             lstate.c
             lauxlib.c
             lapi.h
             ldblib.c
             lgc.h
             lmem.h
             lzio.h
             lualib.h
             )
             

if (WIN32)             
else()
  if(USE_32BITS)
    SET(CMAKE_C_FLAGS "-Wall -ggdb -pipe -march=i386 -mtune=i686 -fPIC")
    SET(CMAKE_CXX_FLAGS "-Wall -ggdb -pipe -march=i386 -mtune=i686 -fPIC")
  else()
    SET(CMAKE_C_FLAGS "-Wall -ggdb -pipe -march=x86-64 -mtune=i686 -fPIC")
    SET(CMAKE_CXX_FLAGS "-Wall -ggdb -pipe -march=x86-64 -mtune=i686 -fPIC")
  endif(USE_32BITS)
endif()


SET(LIBRARY_OUTPUT_PATH ${TF_CURRENT_BINARY_PATH_LIB})

ADD_LIBRARY(lua SHARED ${SRC_LIST} ${BASELIB_LIST})

IF(CMAKE_SYSTEM MATCHES Windows)
  
ENDIF(CMAKE_SYSTEM MATCHES Windows)


