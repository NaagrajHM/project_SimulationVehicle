cmake_minimum_required(VERSION 3.10)

project(SimulationVehicle_v0.0.3)

add_executable(b_${PROJECT_NAME}
	source/Application/Application.cpp
	source/ClassCore/ClassCore.cpp
	source/ClassRingBuffer/ClassRingBuffer.cpp
)

target_include_directories(b_${PROJECT_NAME} PRIVATE
	source/InterfaceCore
	source/ClassRingBuffer
)

