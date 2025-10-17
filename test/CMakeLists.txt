# Simply link against gtest or gtest_main as needed. Eg
#include(CTest)
add_executable(example example.cpp
        example.cpp)
target_link_libraries(example gtest_main)
add_test(NAME example_test COMMAND example)
