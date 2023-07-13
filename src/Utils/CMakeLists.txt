add_library(Utils "")

set_target_properties(Utils PROPERTIES LINKER_LANGUAGE CXX)

target_sources(Utils
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/Utils.inl
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/Utils.h
  )
target_include_directories(Utils
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}
  )