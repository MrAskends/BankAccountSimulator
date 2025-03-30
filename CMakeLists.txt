cmake_minimum_required(VERSION 4.0)

project (BankAccountSimulator LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCES
    source/main.cpp
    source/io.cpp
	source/evaluate.cpp
	source/menu.cpp
)
set(HEADERS
    include/io.h
	include/evaluate.h
	include/menu.h
)

add_executable (BankAccountSimulator ${SOURCES} ${HEADERS})

target_include_directories(BankAccountSimulator PRIVATE include)

source_group("Source Files" FILES ${SOURCES})
source_group("Header Files" FILES ${HEADERS})