# a lua profiler

支持Lua5.3，暂不支持luajit

lua文件中
p = require "profiler"  
p.start()

code ....  

lua文件:
print(p.report())  
C#文件:
_luaEnv.luaEnv.DoString($"print(p.report())");

code ....
print(p.report())
code ...

p.stop()
