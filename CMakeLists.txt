cmake_minimum_required(VERSION 3.16)
project(qt-material-widgets VERSION 1.0 LANGUAGES C CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
include(GNUInstallDirs)

find_package(QT NAMES Qt5 Qt6 REQUIRED COMPONENTS Core)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Gui Widgets)

# 自定义变量：是否启用特定功能
option(ENABLE_EXAMPLES "Enable the examples" OFF)

add_subdirectory(components)
if(ENABLE_EXAMPLES) 
    add_subdirectory(examples)  
else()
    message("examples is disabled.")
endif()

