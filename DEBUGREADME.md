# a lua debugger like gdb

支持Lua5.3，暂不支持luajit

步骤:
 1.  需要生成lua5.3的libxlua.so。
        linux端跑server:  
	    使用 cd xLua/build;  ./make_linux64_lua53.sh;  
	    替换 OrleansLobby/3party/LuaJit/linux_x64/libxlua.so  
	windows端:  
	    右键Sims-> 属性 -> 生成 -> 条件编译和符号输入EnableLuaDebug
 
 3. 打断点  
 	local gdebug = require "gdebug"  
	gdebug.addlinebreak("@behaviour", 136)  --加断点
		
 4. 运行程序,  查看帮助输入h  
	--help  
	 b   --   break line. eg. b file line ...  
                 current file: eg. b line ...  
        c   --   continue  
        n   --   next line  
        s   --   step in  
        o   --   step over  
        l   --   print context lua code. eg. l [lines]  
        p   --   print var value. eg. p var1 var2 ...   
        t   --   traceback  
        pb  --   print all break points  
        cb  --   clear all break points  
        db  --   delete break point. eg. db id1 id2 ...  
        set --   set value. eg. set var value  
