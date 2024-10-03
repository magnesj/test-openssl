cmake_minimum_required(VERSION 3.15)
project(OpenSSL_Mixed)

find_package(OpenSSL REQUIRED)

add_executable(MyExecutable main.cpp)
target_link_libraries(MyExecutable OpenSSL::SSL OpenSSL::Crypto)