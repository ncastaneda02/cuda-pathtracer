# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.11)

project ("cuda-pathtracer")
enable_language(CUDA)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED YES)

set(SOURCE_FILES
	src/pathtracer/pathtracer.cu
	src/pathtracer/materials.cu
	src/pathtracer/camera.cu
	src/pathtracer/sampler.cu
	src/pathtracer/renderer.cu
)

set(HEADER_FILES
	src/pathtracer/pathtracer.h
	src/pathtracer/materials.h
	src/pathtracer/camera.h
	src/pathtracer/sampler.h
	src/pathtracer/renderer.h

)

add_executable(pathtracer ${SOURCE_FILES} ${HEADER_FILES})
set_target_properties(pathtracer PROPERTIES CUDA_ARCHITECTURES native)
