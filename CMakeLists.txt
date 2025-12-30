cmake_minimum_required(VERSION 3.1)
project(test)
 
# 设置 C++ 标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
 
# 添加可执行文件
add_executable(test main.cpp)
 
# 设置 OpenCV 的安装路径（如果有必要的话）
set(OpenCV_DIR "/usr/local/share/opencv4/")
 
# 查找 OpenCV 包
find_package(OpenCV REQUIRED)
 
# 链接 OpenCV 库
target_link_libraries(test PRIVATE ${OpenCV_LIBS})
 
# 包含 OpenCV 的头文件目录
target_include_directories(test PRIVATE ${OpenCV_INCLUDE_DIRS})
 
