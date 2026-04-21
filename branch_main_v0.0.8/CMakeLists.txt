cmake_minimum_required(VERSION 3.10)

project(SimulationVehicle_v0.0.8)

add_executable(b_${PROJECT_NAME}
	source/ClassRingBuffer/ClassRingBuffer.cpp
	source/DeviceDriverEthernet/ClassDeviceDriverEthernet.cpp
	source/ServicesCommunicationDcm/ClassServicesCommunicationDcm.cpp
	source/ServicesSystemEcuM/ClassServicesSystemEcuM.cpp
)

target_include_directories(b_${PROJECT_NAME} PRIVATE
	source/ClassRingBuffer
	source/DeviceDriverEthernet
	source/ServicesCommunicationDcm
	source/ServicesSystemEcuM
	source/ServicesSystemSchM
)
