set(LIB_SRC hello.c)
add_library(hello ${LIB_SRC})
set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib2)
#set_target_properties(hello PROPERTIES OUTPUT_NAME "hello")