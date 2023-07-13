add_library(Print_Utils "")

set_target_properties(Print_Utils PROPERTIES LINKER_LANGUAGE CXX)

target_sources(Print_Utils
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/Print_Utils.inl
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/Print_Utils.h
  )
target_include_directories(Print_Utils
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}
  )