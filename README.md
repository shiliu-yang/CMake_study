# CMake_study

## 常用函数 

```cmake
#最低版本要求
cmake_minimum_required(VERSION 3.16)

#CMake project 为DEMO1，可用${PROJECT_SOURCE_DIR}，${PROJECT_BINARY_DIR}
project(DEMO1)

#设置变量
set(SRC_LIST main.c)

#生成名字为demo1的编译产物
add_executable(demo1 ${SRC_LIST})

#打印信息
message(${PROJECT_SOURCE_DIR})
```

```cmake
#将静态库libhello.lib(liblibhello.a) 重命名为 hello.lib(libhello.a) 
set_target_properties(libhello PROPERTIES OUTPUT_NAME "hello")
```



## 多级目录

文件目录：

```shell
+
|
+--- CMakeLists.txt
+--+ src/
|  |
|  +--- main.c
|  /--- CMakeLists.txt
|
+--+ libhello/
|  |
|  +--- hello.h
|  +--- hello.c
|  /--- CMakeLists.txt
|
/--+ build/
```



顶层CMakeLists.txt：

```cmake
project(HELLO)
add_subdirectory(src)
add_subdirectory(libhello)
```

 

scr中CMakeLists.txt：

```cmake
include_directories(${PROJECT_SOURCE_DIR}/libhello)
set(APP_SRC main.c)
add_executable(hello ${APP_SRC})
target_link_libraries(hello libhello)
```

 

libhello 中CMakeLists.txt：

```cmake
set(LIB_SRC hello.c)
add_library(libhello ${LIB_SRC})
set_target_properties(libhello PROPERTIES OUTPUT_NAME "hello")
```



在build文件夹中:

```shell
$ cmake ..
$ make
$ ./hello
```





## 常用变量

`PROJECT_SOURCE_DIR`和`PROJECT_BINARY_DIR`（需要使用project） 





