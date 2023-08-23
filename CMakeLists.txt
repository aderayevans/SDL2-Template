cmake_minimum_required(VERSION 3.21.1)
# set the project name
project(SDL2_Template VERSION 1.0)

# specify the C++ standard
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS ON)
add_compile_options(
    $<$<CXX_COMPILER_ID:GNU>:-Wno-psabi>
    $<$<CXX_COMPILER_ID:GNU>:-funwind-tables>
    $<$<CXX_COMPILER_ID:GNU>:-fasynchronous-unwind-tables>
)

find_package(SDL2 REQUIRED)
find_package(SDL_image REQUIRED)
find_package(SDL_ttf REQUIRED)

# add the executable
add_executable(${PROJECT_NAME} 
    src/main.cpp
)

target_include_directories(${PROJECT_NAME} PRIVATE 
    include/
    ${SDL2_INCLUDE_DIRS}/
    ${SDL_INCLUDE_DIRS}/
    ${SDL2_IMAGE_INCLUDE_DIRS}/
    ${SDL_IMAGE_INCLUDE_DIRS}/
)

include_directories(${SDL2_INCLUDE_DIRS} ${SDL2_IMAGE_INCLUDE_DIRS})

target_link_libraries(${PROJECT_NAME} 
    ${SDL2_LIBRARIES}
    ${SDL2_IMAGE_LIBRARIES}
)

install(TARGETS ${PROJECT_NAME}
    RUNTIME DESTINATION sbin)
