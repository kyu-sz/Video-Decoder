cmake_minimum_required (VERSION 2.8.7)

project (video_decoder)

set (JAVA_HOME $ENV{JAVA_HOME} CACHE PATH "Home directory of Java Divelooment Toolkit (JDK).")
 
add_subdirectory (jni lib)

set(TEST_VIDEO_PATH CACHE FILEPATH "File path of video for test.")
add_subdirectory(test bin)

install (FILES ${PROJECT_SOURCE_DIR}/include/video_decoder.hpp DESTINATION include/video_decoder)
install (FILES ${PROJECT_SOURCE_DIR}/include/avio_context_manager.h DESTINATION include/video_decoder)
