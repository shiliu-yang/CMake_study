# 对cmake的最低版本要求
cmake_minimum_required(VERSION 3.16)

# cmake project 名字为 DEMO1
project(DEMO1)

# 设置变量
set(SRC_LIST main.c)

# 生成编译产物的名字为demo1
add_executable(demo1 ${SRC_LIST})
