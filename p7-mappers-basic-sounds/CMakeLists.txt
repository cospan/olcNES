project(p7-nes)

find_package(Threads REQUIRED)
find_package(ALSA REQUIRED)

set(CMAKE_BUILD_TYPE Release)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "-g3 -pthread")
set(CMAKE_EXE_LINKER_FLAGS "-lpthread")

#add_compile_definitions(USE_ALSA)
#add_definitions(-DUSE_ALSA)


include_directories(
    "${ALSA_INCLUDE_DIR}"
    )

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
    "Mapper_001.cpp"
    "Mapper_001.h"
    "Mapper_002.cpp"
    "Mapper_002.h"
    "Mapper_003.cpp"
    "Mapper_003.h"
    "Mapper_004.cpp"
    "Mapper_004.h"
    "Mapper_066.cpp"
    "Mapper_066.h"
    "olc2A03.cpp"
    "olc2A03.h"
    "olc2C02.cpp"
    "olc2C02.h"
    "olc6502.cpp"
    "olc6502.h"
    "olcNes_Sounds1.cpp"
		)

add_executable(${PROJECT_NAME} ${SOURCES})


target_link_libraries(
    ${PROJECT_NAME}
		"X11"
		"GL"
		"png"
		"stdc++fs"
    "asound"
		)

#MESSAGE (STATUS "Building Part 2")
#install(TARGETS ${PROJECT_NAME} DESTINATION bin)
