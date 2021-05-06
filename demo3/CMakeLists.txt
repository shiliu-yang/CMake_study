# 对cmake的最低版本要求
cmake_minimum_required(VERSION 3.16)

# cmake project 名字为 DEMO3
project(DEMO3)

# 设置变量
set(SRC_LIST main.c func1.c func2.c)

message(${SRC_LIST})

# 生成编译产物的名字为demo3
add_executable(demo3 ${SRC_LIST})
