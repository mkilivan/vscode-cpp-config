option(ENABLE_DOXYGEN "Enable Doxygen doc builds of source" OFF)

if(ENABLE_DOXYGEN)
  find_package(Doxygen REQUIRED dot)

  set(DOXYGEN_CALLER_GRAPH ON)
  set(DOXYGEN_CALL_GRAPH ON)
  set(DOXYGEN_EXTRACT_ALL ON)
  set(DOXYFILE_IN ${CMAKE_CURRENT_SOURCE_DIR}/Doxyfile.in)
  doxygen_add_docs(doxygen-docs ${PROJECT_SOURCE_DIR})
endif()
