cmake_minimum_required(VERSION 3.21)
project(imgui_demo)

set (SDL_STATIC ON)
add_subdirectory(SDL)
include_directories(. backends SDL/include)

add_executable(imgui_demo examples/example_sdl3_vulkan/main.cpp imgui.cpp imgui_draw.cpp imgui_demo.cpp imgui_tables.cpp imgui_widgets.cpp backends/imgui_impl_sdl3.cpp backends/imgui_impl_vulkan.cpp)

target_link_libraries(imgui_demo SDL3-static vulkan)
