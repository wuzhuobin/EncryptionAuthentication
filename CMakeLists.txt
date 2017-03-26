cmake_minimum_required(VERSION 2.8)
 
PROJECT(EncryptionAuthentication)

find_package(Qt5Widgets REQUIRED)


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

set(
	MAIN_LINK_DIRECTORIES
	${CMAKE_ARCHIVE_OUTPUT_DIRECTORY}
	${CMAKE_LIBRARY_OUTPUT_DIRECTORY}
)

link_directories(
	${MAIN_LINK_DIRECTORIES}
	)

# SET(
# 	MAIN_INCLUDE_DIRS
# 	### Directories for MOC Sources ###

# 	### Directories for headers ###
# 	)

# include_directories(
# 	${MAIN_INCLUDE_DIRS}
# )

# set(
# 	LINK_LIBRARIE
#     Qt5::Widget
# 	EncryptionAuthentication
# )

add_subdirectory(codes/EncryptionAuthentication)