cmake_minimum_required(VERSION 3.21)

project(WebServer)

set(CMAKE_CXX_STANDARD 17)

find_package(Boost REQUIRED COMPONENTS system)

include_directories(include)

add_executable(server src/main.cpp src/utils.cpp)

target_link_libraries(server Boost::system)
