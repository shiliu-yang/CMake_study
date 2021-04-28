include_directories(${PROJECT_SOURCE_DIR}/lib)

set(APP_SRC main.c)
add_executable(demo4 ${APP_SRC})
target_link_libraries(demo4 hello)
