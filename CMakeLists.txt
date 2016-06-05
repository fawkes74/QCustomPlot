cmake_minimum_required(VERSION 3.0)

project(QCustomPlot)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wno-unknown-pragmas")

add_library(${PROJECT_NAME} qcustomplot.cpp qcustomplot.h)

target_link_libraries(${PROJECT_NAME}
	Qt5::Core
    Qt5::PrintSupport
    Qt5::Widgets
)

target_include_directories(${PROJECT_NAME}
  PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
)

set_target_properties(${PROJECT_NAME} PROPERTIES
  AUTOMOC ON
)
