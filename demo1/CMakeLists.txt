#最低版本要求
cmake_minimum_required(VERSION 3.16)

#CMake project 为DEMO1，可用${PROJECT_SOURCE_DIR}，${PROJECT_BINARY_DIR}
project(DEMO1)

#设置变量
set(SRC_LIST main.c)

#生成名字为demo1的编译产物
add_executable(demo1 ${SRC_LIST})
