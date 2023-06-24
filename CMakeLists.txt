cmake_minimum_required(VERSION 3.20)
project(cimplot)

set (CMAKE_CXX_STANDARD 11)

add_definitions(-DIMNODES_NAMESPACE=imnodes)

add_library(cimplot SHARED
    ../cimgui/imgui/imgui.cpp
    ../cimgui/imgui/imgui_draw.cpp
    ../cimgui/imgui/imgui_demo.cpp
    ../cimgui/imgui/imgui_widgets.cpp
	../cimgui/imgui/imgui_tables.cpp
    cimplot.cpp
    implot/implot.cpp
    implot/implot_items.cpp
    implot/implot_demo.cpp)

target_include_directories(cimplot PUBLIC ../cimgui)
target_include_directories(cimplot PUBLIC ../cimgui/imgui)
set_target_properties(cimplot PROPERTIES PREFIX "")

