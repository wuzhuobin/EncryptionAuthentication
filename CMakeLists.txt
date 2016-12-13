cmake_minimum_required(VERSION 2.8)
 
PROJECT(EncryptionAuthentication)

find_package(Qt5Widgets REQUIRED)
# find_package(Qt4 REQUIRED)
# include(${QT_USE_FILE})


# multi-processor build
set(
	CMAKE_CXX_FLAGS 
	"${CMAKE_CXX_FLAGS} /MP"
)

set(
	CMAKE_ARCHIVE_OUTPUT_DIRECTORY
	${CMAKE_SOURCE_DIR}/lib
)

set(
	CMAKE_LIBRARY_OUTPUT_DIRECTORY
	${CMAKE_SOURCE_DIR}/lib
)
set(
	CMAKE_RUNTIME_OUTPUT_DIRECTORY 
	${CMAKE_SOURCE_DIR}/bin
)

link_directories(
	${CMAKE_ARCHIVE_OUTPUT_DIRECTORY}
	${CMAKE_LIBRARY_OUTPUT_DIRECTORY}
	)

SET(
	MAIN_INCLUDE_DIRS
	### Directories for MOC Sources ###

	### Directories for headers ###
	)

include_directories(
	${MAIN_INCLUDE_DIRS}
)

set(
	LINK_LIBRARIE
    Qt5::Core
	EncryptionAuthentication
)

add_subdirectory(codes/EncryptionAuthentication)