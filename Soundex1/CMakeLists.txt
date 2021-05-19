# CMakeList.txt : CMake project for Soundex1, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.14)

project ("Soundex1")


include_directories($ENV{GTEST_HOME}/googletest/include $ENV{GTEST_HOME}/googlemock/include)
link_directories($ENV{GTEST_HOME}/mybuild/lib/MinSizeRel)
add_definitions(-std=c++17)

set(CMAKE_CXX_FLAGS "${CMAXE_CXX_FLAGS} -Wall")

set(sources 
   SoundexTest.cpp)

add_executable(test ${sources})

target_link_libraries(test gmock)
target_link_libraries(test gtest)
