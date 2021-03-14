find_package(Doxygen REQUIRED dot)

option(ENABLE_DOXYGEN "Enable Doxygen doc builds of source" OFF)

if(ENABLE_DOXYGEN)
  if(NOT DOXYGEN_FOUND)
    message(FATAL_ERROR "Doxygen is needed to build the documentation.")
  endif()

  set(DOXYGEN_CALLER_GRAPH YES)
  set(DOXYGEN_CALL_GRAPH YES)
  set(DOXYGEN_EXTRACT_ALL YES)
  set(DOXYGEN_USE_MDFILE_AS_MAINPAGE "README.md")
  set(DOXYGEN_PROJECT_BRIEF "An example of setting up C++ project")

  doxygen_add_docs(doxygen-docs ${PROJECT_SOURCE_DIR} COMMENT "Generating docs")

endif()
