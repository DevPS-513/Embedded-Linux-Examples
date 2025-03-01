cmake_minimum_required(VERSION 2.6)
project(MyProject)

# Find the hello library
find_library(HELLO_LIB NAMES hello PATHS /usr/lib/hello)


include_directories(/usr/local/include/hello)
# link_directories(/usr/lib/hello)
add_executable(myexec src/main.cpp)
target_link_libraries(myexec ${HELLO_LIB})