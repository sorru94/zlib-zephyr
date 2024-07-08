# (C) Copyright 2024, SECO Mind Srl
#
# SPDX-License-Identifier: Apache-2.0

if(CONFIG_ZLIB)

  set(ZLIB_DIR ${ZEPHYR_CURRENT_MODULE_DIR})

  zephyr_library()

  zephyr_include_directories(${ZLIB_DIR})

  FILE(GLOB lib_sources ${ZLIB_DIR}/*.c)
  zephyr_library_sources(${lib_sources})

  zephyr_library_compile_definitions(HAVE_UNISTD_H)

endif()
