# Set the minimum version of CMake that can be used
# To find the cmake version run
# $ cmake --version
cmake_minimum_required(VERSION 3.5)
#set(CMAKE_GENERATOR "MinGW Makefiles" CACHE INTERNAL "" FORCE)
set(CMAKE_MAKE_PROGRAM:PATH C:/MinGW/bin/make.exe)
set(CMAKE_CXX_COMPILER C:/MinGW/bin/g++.exe)#设置C++编译器  
set(CMAKE_C_COMPILER C:/MinGW/bin/gcc.exe) 

MESSAGE(STATUS "CMAKE_CXX_COMPILER:" ${CMAKE_CXX_COMPILER})
MESSAGE(STATUS "CMAKE_C_COMPILER:" ${CMAKE_C_COMPILER})  
MESSAGE(STATUS "CMAKE_MAKE_PROGRAM:" ${CMAKE_MAKE_PROGRAM})   

 
# Set the project name
project (hello_cmake)

# Add an executable
add_executable(hello_cmake main.cpp)

#cmake  -G "MinGW Makefiles" -D"CMAKE_MAKE_PROGRAM:PATH=C:/MinGW/bin/make.exe" ..
