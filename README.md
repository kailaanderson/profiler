# profiler

This profiler project uses a Tree ADT, manipulated by inserting and deleting nodes. 
The profiler is used to present how many times each part of a program is executed.
Implementation includes parsing the source code and generating an abstract syntax tree of the code. Then, the AST can be traversed and once a construct is found, another piece of code keeps track of how many times the function is executed.
srcML is used as a parsing tool in this project. srcML data files are provided, however use "srcml main.cpp -o main.cpp.xml" to generate srcML files for other pieces of code.

Compile and run instructions:
srcml simple.cpp -o simple.cpp.xml
./profiler simple.cpp.xml
clang++ -Wall p-simple.cpp -c
clang++ -Wall profile.cpp -c
clang++ -Wall p-simple.o profile.o -o p-simple
./p-simple
