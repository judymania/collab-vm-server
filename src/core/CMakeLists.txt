# Core library

add_library(collabvm_core
		util/CommandLine.cpp
		VncHack.cpp
		VncHack.h
		PluginManager.cpp
)

target_include_directories(collabvm_core PUBLIC ${PROJECT_SOURCE_DIR}/include)
target_link_libraries(collabvm_core PRIVATE Boost::system)

add_library(collabvm::core ALIAS collabvm_core)

collabvm_targetize(collabvm_core)