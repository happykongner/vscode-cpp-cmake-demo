cmake_minimum_required(VERSION 3.21)
project(helloworld)

set(CMAKE_CXX_STANDARD 17)

# 遍历项目根目录下所有的 .cpp 文件
#file (GLOB files *.cpp)
#foreach (file ${files})
#    string(REGEX REPLACE ".+/(.+)\\..*" "\\1" exe ${file})
#    add_executable (${exe} ${file})
#    message (\ \ \ \ --\ src/${exe}.cpp\ will\ be\ compiled\ to\ bin/${exe})
#endforeach ()
#
#add_executable(test test.h)
#add_executable(main main.cpp)
#
file (GLOB files *.cpp */*.cpp)
foreach (file ${files})
string(REGEX REPLACE ".+/(.+)\\..*" "\\1" exe ${file})
add_executable (${exe} ${file} test/simplex.cpp)
message (\ \ \ \ --\ src/${exe}.cpp\ will\ be\ compiled\ to\ bin/${exe})
endforeach ()