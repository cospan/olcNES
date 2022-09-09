project(p5-nes)

find_package(Threads REQUIRED)

set(CMAKE_BUILD_TYPE Release)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "-g3 -pthread")
set(CMAKE_EXE_LINKER_FLAGS "-lpthread")

set(SOURCES
    "Bus.cpp"
    "Bus.h"
    "Cartridge.cpp"
    "Cartridge.h"
    "CMakeLists.txt"
    "Mapper.cpp"
    "Mapper.h"
    "Mapper_000.cpp"
    "Mapper_000.h"
    "olc2C02.cpp"
    "olc2C02.h"
    "olc6502.cpp"
    "olc6502.h"
    "olcNes_PPU_Foregrounds.cpp"
		)

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(
    ${PROJECT_NAME}
		"X11"
		"GL"
		"png"
		"stdc++fs"
		)

#MESSAGE (STATUS "Building Part 2")
#install(TARGETS ${PROJECT_NAME} DESTINATION bin)
