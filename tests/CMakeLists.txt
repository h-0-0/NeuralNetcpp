include(FetchContent)

FetchContent_Declare(
  googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG        release-1.11.0
)
FetchContent_MakeAvailable(googletest)
add_library(GTest::GTest INTERFACE IMPORTED)
target_link_libraries(GTest::GTest INTERFACE gtest_main)


add_executable(Unit_Tests Unit_Tests.cpp)

target_link_libraries(Unit_Tests
  GTest::GTest
  Neural_Net
  Optimizer
  Print_Utils
  Utils
)

# add_test(Unit_Tests_gtests Unit_Tests)

add_test(
  NAME
    Unit_Tests
  COMMAND
    $<TARGET_FILE:Unit_Tests>
  )