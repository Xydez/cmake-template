cmake_minimum_required(VERSION 3.10)

# Add the project
project(template
	VERSION 0.0.1
	DESCRIPTION "Template CMake project"
	LANGUAGES CXX
)

# Add the source files
set(PROJECT_HEADERS
	"include/math.hpp"
)

set(PROJECT_SOURCES
	"src/main.cpp"
	"src/math.cpp"
)

add_executable(template ${PROJECT_SOURCES})

set_target_properties(template PROPERTIES
	CXX_STANDARD 17
	CXX_STANDARD_REQUIRED true
)

target_include_directories(template PUBLIC ${PROJECT_SOURCE_DIR}/include)
