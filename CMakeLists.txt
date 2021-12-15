project(EigenTorials)
cmake_minimum_required(VERSION 3.10)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)
set(EIGEN3_INCLUDE_DIR "/home/qinyu/codes/third_party/eigen")
find_package(Eigen3 REQUIRED)
add_executable(totorial ${CMAKE_CURRENT_SOURCE_DIR}/examples/init.cc)
target_include_directories(totorial PRIVATE ${EIGEN3_INCLUDE_DIR}
                                            ${CMAKE_CURRENT_SOURCE_DIR})