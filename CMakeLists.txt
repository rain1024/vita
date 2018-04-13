cmake_minimum_required(VERSION 3.10)
project(vita)

set(CMAKE_CXX_STANDARD 11)

include_directories(src/dictionary)
include_directories(src/include)
include_directories(src/option_parser)
include_directories(src/text2feat)
include_directories(src/text_util)
include_directories(src/vita)
include_directories(src/vita_ana)
include_directories(src/vncommon)
include_directories(src/vncommon_py)

add_executable(vita
        doc/lab_format.pdf
        src/dictionary/dictionary.cpp
        src/dictionary/dictionary.h
        src/dictionary/test_dictionary.cpp
        src/include/crfsuite.h
        src/include/crfsuite.hpp
        src/include/crfsuite_api.hpp
        src/include/os.h
        src/option_parser/OptionParser.cpp
        src/option_parser/OptionParser.h
        src/text2feat/text2feat.cpp
        src/text2feat/text2feat.h
        src/text_util/text_util.cpp
        src/text_util/text_util.h
        src/text_util/text_util_test.cpp
        src/vita/vita.cpp
        src/vita/vita.h
        src/vita_ana/vita_ana.cpp
        src/vita_ana/vita_ana.h
        src/vita_ana/vita_ana_server.cpp
        src/vncommon/logging.cpp
        src/vncommon/vncommon.cpp
        src/vncommon/vncommon.h
        src/vncommon/vncommon_test.cpp
        src/vncommon_py/logging.cpp
        src/vncommon_py/text_util.cpp
        src/vncommon_py/text_util.h
        src/vncommon_py/vncommon.cpp
        src/vncommon_py/vncommon.h
        src/vncommon_py/vncommon.i
        install_depend.sh
        README.md)
