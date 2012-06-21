
cmake_minimum_required(VERSION 2.8.7)

set(MODULE_NAME MinimalistiCli)

if(NOT Slicer_SOURCE_DIR)
  find_package(Slicer REQUIRED)
  include(${Slicer_USE_FILE})
endif()

SEMMacroBuildCLI(
  NAME ${EXTENSION_NAME}
  TARGET_LIBRARIES ${ITK_LIBRARIES}
  EXECUTABLE_ONLY
  )

