cmake_minimum_required(VERSION 2.8)
project(MegaPro CXX)

# Download automatically, you can also just copy the conan.cmake file
#if(NOT EXISTS "${CMAKE_BINARY_DIR}/conan.cmake")
#   message(STATUS "Downloading conan.cmake from https://github.com/conan-io/cmake-conan")
#   file(DOWNLOAD "https://github.com/conan-io/cmake-conan/raw/v0.14/conan.cmake"
#                 "${CMAKE_BINARY_DIR}/conan.cmake")
#endif()

#include(${CMAKE_BINARY_DIR}/conan.cmake)

#conan_cmake_run(REQUIRES Hello/0.1@memsharded/testing
#                BASIC_SETUP 
#                BUILD missing)

# Add an executable with the above sources
add_executable(mega_bin 
    main.cpp
)

# link the new hello_library target with the hello_binary target
target_link_libraries( mega_binary
    PRIVATE 
        mega_library
)

#target_link_libraries(main ${CONAN_LIBS})