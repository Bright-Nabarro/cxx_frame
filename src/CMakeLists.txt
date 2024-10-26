file(GLOB SRC "*.cpp")

add_executable(${CMAKE_PROJECT_NAME} ${SRC})

ChgExeOutputDir(${CMAKE_PROJECT_NAME})

target_include_directories(${CMAKE_PROJECT_NAME} PUBLIC
	"$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/easylog>"
    "$<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}/easylog>"
)

#include(Doxygen)
#Doxygen("${CMAKE_CURRENT_SOURCE_DIR}/app" "${CMAKE_SOURCE_DIR}/docs")
#
#include(Install)

