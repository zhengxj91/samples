include_directories (
  ${CMAKE_SOURCE_DIR}/sample_common/include
  ${CMAKE_SOURCE_DIR}/sample_multi_transcode/include
  ${CMAKE_SOURCE_DIR}/sample_plugins/vpp_plugin/include
  ${CMAKE_SOURCE_DIR}/sample_plugins/rotate_cpu/include
)

list( APPEND LIBS_VARIANT sample_common )
list( APPEND LIBS_NOVARIANT vpp_plugin )

set(DEPENDENCIES libmfx dl pthread)
make_executable( shortname universal )
