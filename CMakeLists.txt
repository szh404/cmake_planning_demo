cmake_minimum_required(VERSION 3.29.0)
project(planning
    VERSION 0.0.1
    DESCRIPTION "a demo of cmake planning"
    HOMEPAGE_URL "https://github.com/szh404/cmake_planning_demo"
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 17)

# 变量设置
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)
set(Process_Dir ${PROJECT_SOURCE_DIR}/src/process)
set(Pncmap_Dir ${PROJECT_SOURCE_DIR}/src/pnc_map)

# 添加子目录
# 变量会传递到子目录中，相当于继承
add_subdirectory(src) 
