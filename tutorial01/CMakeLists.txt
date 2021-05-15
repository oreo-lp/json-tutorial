cmake_minimum_required (VERSION 2.6)
project (leptjson_test C)

if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -ansi -pedantic -Wall")
endif()
# 生成动态库或者静态库
add_library(leptjson leptjson.c)
# 生成可执行文件
add_executable(leptjson_test test.c)
# 将目标文件和库文件进行链接
target_link_libraries(leptjson_test leptjson)
