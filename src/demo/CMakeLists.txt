file(GLOB_RECURSE demo RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.cpp *.hpp)

add_executable(demo
  ${demo}
)

target_precompile_headers(demo
PRIVATE
  ${CMAKE_CXX_PCH}
)

target_create_vcxproj_filters(demo)
