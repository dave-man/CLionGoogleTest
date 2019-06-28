cmake_minimum_required(VERSION 3.14)
project(CLionGoogleTest)


set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "-std=c++11 -pthread")
include_directories(/usr/local/include)
link_directories(/usr/local/lib)

#Define your executable
add_executable(${PROJECT_NAME} main.cpp)

#Link with GoogleTest
target_link_libraries(${PROJECT_NAME} libgtest.a libgtest_main.a)
#Link with GoogleMock
target_link_libraries(${PROJECT_NAME} libgmock.a libgmock_main.a)

