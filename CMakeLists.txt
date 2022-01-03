cmake_minimum_required(VERSION 3.21)
project(helloworld)

set(CMAKE_CXX_STANDARD 17)

file (GLOB files *.cpp */*.cpp)
foreach (file ${files})
string(REGEX REPLACE ".+/(.+)\\..*" "\\1" exe ${file})
add_executable (${exe} ${file})
message (\ \ \ \ --\ src/${exe}.cpp\ will\ be\ compiled\ to\ bin/${exe})
endforeach ()