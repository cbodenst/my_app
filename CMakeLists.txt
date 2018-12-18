project(pkg_sample)
cmake_minimum_required(VERSION 2.8)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -D_FORCE_INLINES")

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

add_executable(pkgsample sample.cpp)

install (FILES 
	${CMAKE_BINARY_DIR}/pkgsample
	PERMISSIONS OWNER_EXECUTE OWNER_WRITE OWNER_READ WORLD_EXECUTE WORLD_READ GROUP_EXECUTE GROUP_READ
	DESTINATION bin)

