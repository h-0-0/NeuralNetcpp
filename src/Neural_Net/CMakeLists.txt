include_directories(${NeuralNetcpp_SOURCE_DIR}/src/Print_Utils)
include_directories(${NeuralNetcpp_SOURCE_DIR}/src/Utils)

add_library(Neural_Net "")

target_sources(Neural_Net
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/Neural_Net.cpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/Neural_Net.h
  )
target_include_directories(Neural_Net
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}
  )