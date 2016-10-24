cmake_minimum_required(VERSION 2.8) 
PROJECT (bsnake_lane_detection)

add_definitions ("-w")
find_package(OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

set( NAME_SRC
    src/main.cpp
)

set( NAME_HEADERS       
     include/utils.h
)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR})

add_executable(filter src/main.cpp)
target_link_libraries(filter ${OpenCV_LIBRARIES})