PROJECT(CaPTk_IO)

#SET( CMAKE_ARCHIVE_OUTPUT_DIRECTORY 
#	${CaPTk_BINARY_DIR})
  
SET( ${PROJECT_NAME}_HDRS
  ${PROJECT_SOURCE_DIR}/inc/DicomSeriesReader.h
  ${PROJECT_SOURCE_DIR}/inc/DicomMetadataReader.h
  ${PROJECT_SOURCE_DIR}/inc/DicomIOManager.h
  ${PROJECT_SOURCE_DIR}/inc/DicomIOManager.hxx
  ${PROJECT_SOURCE_DIR}/inc/DicomImageReader.h
)

SET( ${PROJECT_NAME}_SRCS
  ${PROJECT_SOURCE_DIR}/src/DicomSeriesReader.cpp
  ${PROJECT_SOURCE_DIR}/src/DicomMetadataReader.cpp
  ${PROJECT_SOURCE_DIR}/src/DicomImageReader.cpp
)

SET( ${PROJECT_NAME}_HDRS "${${PROJECT_NAME}_HDRS}" CACHE STRING "Dicom IO headers" FORCE )
SET( ${PROJECT_NAME}_SRCS "${${PROJECT_NAME}_SRCS}" CACHE STRING "Dicom IO sources" FORCE )
                     
INCLUDE_DIRECTORIES( 
${CMAKE_CURRENT_SOURCE_DIR}/inc
)

SET( CACHED_INCLUDE_DIRS 
  ${CACHED_INCLUDE_DIRS}
  ${CMAKE_CURRENT_SOURCE_DIR}/inc
  CACHE STRING "All include directories" FORCE
)
  
#IF(NOT (TARGET CaPTk_IO))
  
#  ADD_LIBRARY(
#    ${PROJECT_NAME}
#    ${${PROJECT_NAME}_SRCS}
#    ${${PROJECT_NAME}_HDRS}
#  )

#  TARGET_LINK_LIBRARIES( ${PROJECT_NAME} ${ITK_LIBRARIES} )
  
#ENDIF()
