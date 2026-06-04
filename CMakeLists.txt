cmake_minimum_required(VERSION 3.16)
project(MemoRe VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 REQUIRED COMPONENTS Quick)

qt_standard_project_setup()

qt_add_executable(appMemoRe
    src/main.cpp
)

qt_add_qml_module(appMemoRe
    URI MemoRe
    VERSION 1.0
    QML_FILES
        src/Main.qml
)

target_link_libraries(appMemoRe
    PRIVATE Qt6::Quick
)
