CU_SET_PATH("CMAKE_TRANSM_SRC_DIR" "${CMAKE_CURRENT_LIST_DIR}")

AC_ADD_SCRIPT("${CMAKE_TRANSM_SRC_DIR}/transmog_scripts.cpp")
AC_ADD_SCRIPT("${CMAKE_TRANSM_SRC_DIR}/Transmogrification.cpp")

CU_ADD_HOOK(AFTER_WORLDSERVER_CMAKE "${CMAKE_TRANSM_SRC_DIR}/cmake/after_ws.cmake")

AC_ADD_SCRIPT_LOADER("Transmog" "${CMAKE_TRANSM_SRC_DIR}/transmog_scripts_loader.h")
