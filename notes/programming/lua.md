Lua is a great, tiny, embeddable language.

It is designed primarily around the table data structure.

In your C source, you will need to include the lua header: 

Each function you wish to export is written with the same types:

And add a stub function that returns the function table:

You need to compile your C source as a shared library:



Having done all that, in lua you should be able to load up the module.

[Torch | Scientific computing for LuaJIT.](http://torch.ch/)

