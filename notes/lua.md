Lua is a great, tiny, embeddable language.

It is designed primarily around the table data structure.

In your C source, you will need to include the lua header: 

#include <lua5.2/lua.h>

#include <lua5.2/lauxlib.h>



Each function you wish to export is written with the same types:

static int l_listen(lua_State *L)



And add a stub function that returns the function table:

static const struct luaL_Reg conkyhttpd [] = {

    {"listen", l_listen},

    {"setup", l_setup},

    {"cleanup", l_cleanup},

    {NULL, NULL}  /* sentinel */

};



int luaopen_conkyhttpd(lua_State *L)

{

    luaL_openlib(L, "conkyhttpd", conkyhttpd, 0);

    return 1;

}



You need to compile your C source as a shared library:

gcc -llua5.2 -fPIC -shared -o webconky.so webconky.c



Having done all that, in lua you should be able to load up the module.

require(webconky)

--alternatively, load it manually

mylib = loadlib("fullname-of-your-library", "luaopen_mylib")

mylib()

[Torch | Scientific computing for LuaJIT.](http://torch.ch/)

