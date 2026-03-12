cmake_minimum_required(VERSION 3.10)

project(SimulationVehicle_v0.0.1)

add_executable(${PROJECT_NAME}
	source/Application/Application.cpp
	source/ClassCore/ClassCore.cpp
)

target_include_directories(${PROJECT_NAME} PRIVATE
	source/InterfaceCore
)

