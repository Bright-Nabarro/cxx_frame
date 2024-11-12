file(GLOB SRC "*.cpp")

set(trg ${CMAKE_PROJECT_NAME})
add_executable(${trg} ${SRC})

include(Utils)
ChgExeOutputDir(${trg})

target_include_directories(${trg} PUBLIC
	"$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/${trg}>"
    "$<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}/${trg}>"
)



#include(Doxygen)
#Doxygen("${CMAKE_CURRENT_SOURCE_DIR}/app" "${CMAKE_SOURCE_DIR}/docs")
#
#include(Install)

