cmake_minimum_required(VERSION 3.14)
project(googletest)

# GoogleTest requires at least C++11
set(CMAKE_CXX_STANDARD 11)

include(FetchContent)
FetchContent_Declare(
  googletest
  URL https://github.com/google/googletest/archive/8d51dc50eb7e7698427fed81b85edad0e032112e.zip
)
# For Windows: Prevent overriding the parent project's compiler/linker settings
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)

enable_testing()

add_executable(
  sample1
  sample1.cc
  sample1_unittest.cc
)
target_link_libraries(
  sample1
  gtest_main
)

include(GoogleTest)
gtest_discover_tests(sample1)
