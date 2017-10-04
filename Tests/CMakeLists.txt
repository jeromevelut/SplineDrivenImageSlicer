### Find VTK
find_package(VTK REQUIRED)
include(${VTK_USE_FILE})

ADD_EXECUTABLE( testFrenetSerretFrame testFrenetSerretFrame.cxx
              )
TARGET_LINK_LIBRARIES( 
                       testFrenetSerretFrame
                       vtkSDIS
                       ${VTK_LIBRARIES}
                     )

ADD_TEST( testFrenetSerretFrame ${EXECUTABLE_OUTPUT_PATH}/testFrenetSerretFrame )

ADD_EXECUTABLE( testSplineDriveImageSlicer testSplineDriveImageSlicer.cxx
              )
TARGET_LINK_LIBRARIES( 
                       testSplineDriveImageSlicer
                       vtkSDIS
                       ${VTK_LIBRARIES}
                     )

ADD_TEST( testSplineDriveImageSlicer ${EXECUTABLE_OUTPUT_PATH}/testSplineDriveImageSlicer )


