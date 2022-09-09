cmake_minimum_required (VERSION 3.22)


project(NES)


include_directories(
    "${CMAKE_SOURCE_DIR}/submodules/olcPixelGameEngine/Extensions"
    "${CMAKE_SOURCE_DIR}/submodules/olcPixelGameEngine"
		)


add_subdirectory("${CMAKE_SOURCE_DIR}/p2-cpu")
add_subdirectory("${CMAKE_SOURCE_DIR}/p3-buses-ramps-roms-mappers")
add_subdirectory("${CMAKE_SOURCE_DIR}/p4-ppu-backgrounds")
add_subdirectory("${CMAKE_SOURCE_DIR}/p5-ppu-foregrounds")
add_subdirectory("${CMAKE_SOURCE_DIR}/p7-mappers-basic-sounds")

