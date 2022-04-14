project(Choreograph)

cmake_minimum_required (VERSION 3.9) 

# Dependencies that are auto-downloaded, built, and installed for you will go here.  So, you 
# may use this even if not planning to install this particular project on your system.
if (CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT OR "${CMAKE_INSTALL_PREFIX}" STREQUAL "")
    set (CMAKE_INSTALL_PREFIX "${CMAKE_BINARY_DIR}/install" CACHE PATH "default install path" FORCE )
endif()


if(COMMAND cmake_policy)
  cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

	


add_library(Choreograph STATIC
	choreograph/Choreograph.h
	choreograph/Cue.cpp
	choreograph/Cue.h
	choreograph/Easing.h
	choreograph/Motion.hpp
	choreograph/Output.hpp
	choreograph/Phrase.hpp
	choreograph/Sequence.hpp
	choreograph/Timeline.cpp
	choreograph/Timeline.h
	choreograph/TimelineItem.cpp
	choreograph/TimelineItem.h
	choreograph/TimelineOptions.hpp
	choreograph/TimeType.h
	choreograph/detail/MakeUnique.hpp
	choreograph/detail/VectorManipulation.hpp
	choreograph/phrase/Combine.hpp
	choreograph/phrase/Hold.hpp
	choreograph/phrase/Procedural.hpp
	choreograph/phrase/Ramp.hpp
	choreograph/phrase/Retime.hpp
	choreograph/phrase/Sugar.hpp
	
)

target_include_directories(Choreograph PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
)
