include_directories(${PROJECT_SOURCE_DIR}/lib)

set(APP_SRC main.c)
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
add_executable(demo5 ${APP_SRC})
target_link_libraries(demo5 hello)
