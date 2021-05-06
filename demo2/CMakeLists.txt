# 对cmake的最低版本要求
cmake_minimum_required(VERSION 3.16)

# cmake project 名字为 DEMO2
project(DEMO2)

# 设置变量
set(SRC_LIST main.c)

# 生成编译产物的名字为demo2
add_executable(demo2 ${SRC_LIST})
