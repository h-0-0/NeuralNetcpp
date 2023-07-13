add_library(Optimizer "")

set_target_properties(Optimizer PROPERTIES LINKER_LANGUAGE CXX)

target_sources(Optimizer
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/Optimizer.tpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/Optimizer.h
  )
target_include_directories(Optimizer
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}
  )