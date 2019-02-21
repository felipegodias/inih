message(STATUS "Inih examples enabled.")

project(dump)
add_executable(dump ini_dump.c)
target_link_libraries(dump inih)

project(example)
add_executable(example ini_example.c)
target_link_libraries(example inih)

project(xmacros)
add_executable(xmacros ini_xmacros.c)
target_link_libraries(xmacros inih)

project(example_cpp)
add_executable(example_cpp ini_reader_example.cpp)
target_link_libraries(example_cpp inih)
