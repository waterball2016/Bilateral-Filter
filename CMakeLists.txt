CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT( beauty )
INCLUDE_DIRECTORIES( 
	include
	/usr/include
	/usr/include/ImageMagick
	)
AUX_SOURCE_DIRECTORY( src DIR_SRCS )
SET(LIBRARIES
	GLEW
	glut
	GLU
	GL
	X11
	Xext
	Xi
	m
	Magick++
)
ADD_EXECUTABLE(beauty ${DIR_SRCS})
TARGET_LINK_LIBRARIES(beauty ${LIBRARIES})
