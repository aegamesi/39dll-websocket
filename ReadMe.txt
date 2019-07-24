License for modifications: GNU GPLv3

Source code for 39dll.
main.cpp only contains code to port the functions/classes to game maker.
the classes can also be used within ur c++ projects.
All the code was made by 39ster (except for the 1 or 2 functions that are commented)

//How to compile with code::blocks
Open the 39DLL.cbp file and press compile.
If you do not have Code::Blocks than download it for free at http://www.codeblocks.org/

//How to compile without code::blocks (untested)
Compile all the .cpp files and link with iphlpapi.lib, wininet.lib, wsock32.lib

============= BUILDING: =============

Use Docker and dockcross to build on any platform.
First: `docker run --rm dockcross/windows-static-x86 > ./dockcross`

Then `./dockcross bash`, and finally run:

$CXX -shared *.cpp -lwsock32 -lwininet -liphlpapi -o 39dll_ws.dll
