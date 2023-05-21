# CMakeList.txt : CMake project for cuda-pathtracer, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

# Add source to this project's executable.
add_executable (cuda-pathtracer "cuda-pathtracer.cpp" "cuda-pathtracer.h")

# TODO: Add tests and install targets if needed.
