cmake_minimum_required (VERSION 2.8)

project (studiolibrary NONE)
set (CMAKE_INSTALL_MESSAGE LAZY)

install (DIRECTORY src/ DESTINATION "${CMAKE_INSTALL_PREFIX}"
  USE_SOURCE_PERMISSIONS
  PATTERN "data/test" EXCLUDE
  PATTERN "*.pyc" EXCLUDE
  PATTERN "__pycache__" EXCLUDE
)

install(FILES info.json DESTINATION "${CMAKE_INSTALL_PREFIX}")
