project(planning_main)

add_subdirectory(pnc_map)
add_subdirectory(process)

# 因为main,cpp在这一层，所以将其添加为可执行文件
add_executable(${PROJECT_NAME} planning_main.cpp)

target_include_directories(
    ${PROJECT_NAME}
    PUBLIC
    ${Process_Dir}
)

target_link_libraries(
    ${PROJECT_NAME}
    PUBLIC
    process
)