cmake_minimum_required(VERSION 3.16)
project(OptionPricer LANGUAGES CXX)

# TODO: C++17 obligatoire, sans extensions GNU
#       (3 variables CMAKE_CXX_...)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)  # pour l'autocomplétion de VSCode/clangd

# --- Bibliothèque : le cœur du pricer ---
# TODO: add_library(pricer_lib STATIC ...)
# TODO: include/ en PUBLIC
# TODO: warnings -Wall -Wextra -Wpedantic en PRIVATE

# --- Application ---
# TODO: add_executable(pricer_app ...) + linker pricer_lib


# --- Tests ---
include(FetchContent)
FetchContent_Declare(doctest
  GIT_REPOSITORY https://github.com/doctest/doctest.git
  GIT_TAG v2.4.11)
FetchContent_MakeAvailable(doctest)
# TODO: enable_testing(), un exécutable pricer_tests,
#       le linker à pricer_lib ET à doctest::doctest, puis add_test(...)