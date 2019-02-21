message(STATUS "Inih tests enabled.")

project(unittest)
add_executable(unittest unittest.c)
target_link_libraries(unittest inih)