
list( APPEND SOURCE_tests property.test.cpp )
list( APPEND SOURCE_tests main.cpp )

add_executable( bindey-test ${SOURCE_tests} )
target_link_libraries(
  bindey-test
  PRIVATE
    bindey
    Catch2::Catch2
)

set_target_properties(
  bindey-test
  PROPERTIES
    CXX_STANDARD 11
    CXX_EXTENSIONS off
)
