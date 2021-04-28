project(demo3)

#设置变量
set(APP_SRC main.c)
set(LIB_SRC hello.c)

#生成名字为hello的库
add_library(hello ${LIB_SRC})

#编译产物
add_executable(demo3 ${APP_SRC})

#库连接
target_link_libraries(demo3 hello)

#更改lib名字
set_target_properties(hello PROPERTIES OUTPUT_NAME "my_hello")