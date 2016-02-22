AUX_SOURCE_DIRECTORY(. SRC_LIST)
LINK_DIRECTORIES(/Users/cszixin/cmake/demo/cmake/t3/build/lib) # 这行一定要在ADD_EXECUTABLE前面
ADD_EXECUTABLE(t4 ${SRC_LIST})
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

SET(CAME /Users/cszixin/cmake/demo/cmake) # cmake文件夹的位置
INCLUDE_DIRECTORIES(${CAME}/t3/lib_hello/)
TARGET_LINK_LIBRARIES(t4 hello) # 链接动态库
#TARGET_LINK_LIBRARIES(t4 libhello.a) # 链接静态库
