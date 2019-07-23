# Lua-tools  
lua死循环检测：  
需要lua5.3环境  
sims.toml开启EnableCheckLuaInfiniteLoop = true  

https://github.com/Tencent/xLua/blob/master/Assets/XLua/Doc/compatible_bytecode.md

统计Lua使用的内存量:
double MemCount = (double)lua_gc(L, LUA_GCCOUNTB, 0) + (double)(lua_gc(L, LUA_GCCOUNT, 0) * 1024);
