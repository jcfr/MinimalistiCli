
cmake_minimum_required(VERSION 2.8.7)

if(POLICY CMP0017)
  cmake_policy(SET CMP0017 OLD)
endif()

set(EXTENSION_NAME MinimalistiCli)

if(NOT Slicer_SOURCE_DIR)
  find_package(Slicer REQUIRED)
  include(${Slicer_USE_FILE})
endif()

slicerMacroBuildCLI(
  NAME ${EXTENSION_NAME}
  TARGET_LIBRARIES ${ITK_LIBRARIES}
  EXECUTABLE_ONLY
  )

