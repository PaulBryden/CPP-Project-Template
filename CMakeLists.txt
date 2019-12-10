cmake_minimum_required(VERSION 3.15)
project(CPP_Template_Project)

set(CMAKE_CXX_STANDARD 20)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

include_directories(include)
add_executable(CPP_Template_Project src/main.cpp)

enable_testing() # Must be in main file

include(AddGoogleTest) # Google Test CMAKE File
add_executable(SimpleTest  Unit-Tests/SimpleTest.cpp)
add_gtest(SimpleTest)