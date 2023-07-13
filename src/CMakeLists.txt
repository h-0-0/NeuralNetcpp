add_executable(train_net main.cpp)
  
add_subdirectory(Neural_Net)
add_subdirectory(Optimizer)
add_subdirectory(Utils)
add_subdirectory(Print_Utils)

target_link_libraries(train_net
  PRIVATE
    Neural_Net
    Optimizer
    Print_Utils
)
