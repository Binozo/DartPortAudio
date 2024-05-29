cmake_minimum_required(VERSION 3.7 FATAL_ERROR)
project(dart_port_audio VERSION 1.0.0 LANGUAGES CXX)
add_library(dart_port_audio SHARED port_audio_helper.cpp hello.def)

set_target_properties(dart_port_audio PROPERTIES
        PUBLIC_HEADER port_audio_helper.h
        VERSION ${PROJECT_VERSION}
        SOVERSION 1
        OUTPUT_NAME "port_audio"
        XCODE_ATTRIBUTE_CODE_SIGN_IDENTITY "Hex_Identity_ID_Goes_Here"
)