#
# This file was genared by ../proj2cmake/build/proj2cmake and will be overwritten on it's next run!
# Please put all configurations in the cmake_conf/*.cmake files.
#

cmake_minimum_required(VERSION 2.8)

PROJECT(leveldb NONE)
SET(CMAKE_CXX_STANDARD 14)

ADD_DEFINITIONS(-Ofast -DNDEBUG -DWIN32 -DDLLX=__declspec(dllexport) -DLEVELDB_PLATFORM_WINDOWS)

INCLUDE("${leveldb_SOURCE_DIR}/cmake_conf/leveldb.cmake")

INCLUDE("leveldb.cmake")

ADD_LIBRARY(leveldb SHARED
            ${leveldb_SRC})

TARGET_LINK_LIBRARIES(leveldb
            ${leveldb_DEPS}
            ${leveldb_ADDITIONAL_DEPS}
            ${SOLUTION_SHARED_LIB_DEPS}
            ${SOLUTION_GENERAL_DEPS})

