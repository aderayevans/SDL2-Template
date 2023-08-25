cmake_minimum_required(VERSION 3.21.1)
project(SDL2_Template VERSION 1.0)

# Make sure to add the CMAKE_CXX_STANDARD declarations above the call to add_executable()
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS ON)
add_compile_options(
    $<$<CXX_COMPILER_ID:GNU>:-Wno-psabi>
    $<$<CXX_COMPILER_ID:GNU>:-funwind-tables>
    $<$<CXX_COMPILER_ID:GNU>:-fasynchronous-unwind-tables>
)

add_executable(${PROJECT_NAME} 
    src/main.cpp
)

include(FindPkgConfig)

PKG_SEARCH_MODULE(SDL2 REQUIRED sdl2)
PKG_SEARCH_MODULE(SDL2_IMAGE REQUIRED SDL2_image>=2.0.0)

target_include_directories(${PROJECT_NAME} PRIVATE 
    include
    "${PROJECT_BINARY_DIR}"
    ${SDL2_INCLUDE_DIRS}
    ${SDL2_IMAGE_INCLUDE_DIRS}
)

target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARIES} ${SDL2_IMAGE_LIBRARIES})
