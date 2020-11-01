cmake_minimum_required(VERSION 3.15)
project(Opencv4)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV 4.4.0 REQUIRED)
message("OPENCV version is ${OpenCV_VERSION}")

include_directories(${OpenCV_INCLUDE_DIRS} ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_SOURCE_DIR}/includes)
link_directories(${OpenCV_LIB_DIR})

add_executable(Opencv4 main.cpp)
target_link_libraries(Opencv4 ${OpenCV_LIBS})