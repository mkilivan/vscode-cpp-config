option(ENABLE_DOXYGEN "Enable Doxygen doc builds of source" OFF)

if(ENABLE_DOXYGEN)
  find_package(Doxygen REQUIRED dot)

  set(DOXYGEN_CALLER_GRAPH ON)
  set(DOXYGEN_CALL_GRAPH ON)
  set(DOXYGEN_EXTRACT_ALL ON)
  set(DOXYGEN_PROJECT_BRIEF "An example of setting up C++ project")

  doxygen_add_docs(doxygen-docs ${PROJECT_SOURCE_DIR})
endif()
