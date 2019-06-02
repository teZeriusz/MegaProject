cmake_minimum_required(VERSION 3.13)


############################################################
# Create a library
############################################################

#Generate the static library from the library sources
add_library(mega_library STATIC 
    mega.cpp
)

target_include_directories(mega_library
    PUBLIC 
        ${PROJECT_SOURCE_DIR}/src/mega
)