cmake_minimum_required(VERSION 2.8)
project(HttpRouter)

include_directories(include)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -fPIC")

set(SOURCE_FILES
        include/HttpHandlers.h
        include/HttpRouter.h
        src/HttpHandlers.cpp
        src/HttpRouter.cpp)

# add_executable(HttpRouter ${SOURCE_FILES})
add_library(PocoHttpRouter ${SOURCE_FILES})
target_include_directories(PocoHttpRouter SYSTEM INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/include")
# target_link_libraries(HttpRouter PocoFoundation
#     PocoNetSSL
#     PocoUtil
#     PocoCrypto
#     PocoNet
#     PocoXML)
