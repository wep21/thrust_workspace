cmake_minimum_required(VERSION 3.18)
project(thrust_workspace)

include(CheckLanguage)
check_language(CUDA)
if(NOT CMAKE_CUDA_COMPILER)
  message(WARNING "CUDA not found")
  return()
endif()

enable_language(CUDA)

add_executable(minmax
  src/minmax.cu
)
