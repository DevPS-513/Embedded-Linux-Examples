cmake_minimum_required(VERSION 2.6)
project(MyProject)
add_library(hello SHARED src/hello.cpp)

# Specify the installation directories
install(TARGETS hello
        LIBRARY DESTINATION /usr/lib/hello)

# Specify the installation directory for the header file
install(FILES src/hello.hpp
        DESTINATION /usr/local/include/hello)