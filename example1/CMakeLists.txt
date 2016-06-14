#include_directories(/usr/include/libxml2)
#include_directories(${LIBXML2_INCLUDE_DIR})
#include(${CMAKE_SOURCE_DIR}/common.cmake)
add_executable(example1 example1.c)
message(INFO ${Glib_LIBRARIES} ${GSTREAMER_LIBRARIES})
target_link_libraries(
	example1
	${Glib_LIBRARIES}
	${GSTREAMER_LIBRARIES}
	${GOBJECT_LIBRARIES}
	${LIBXML2_LIBRARIES}
)
