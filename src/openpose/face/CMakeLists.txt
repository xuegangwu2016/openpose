set(SOURCES
    defineTemplates.cpp
    faceDetector.cpp
    faceDetectorOpenCV.cpp
    faceExtractor.cpp
    faceCpuRenderer.cpp
    faceGpuRenderer.cpp
    renderFace.cpp
    renderFace.cu
)

cuda_add_library(face ${SOURCES})
if (BUILD_CAFFE)
  add_dependencies(face caffe)
endif (BUILD_CAFFE)
