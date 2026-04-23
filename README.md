# project_SimulationVehicle
Repository for Vehicle Simulation.

# 2026.04.22: branch_main_v0.0.9
Feature:
      #3 Bootloader gets application-like personality.
   ,  #4 Separated driver initialization lists for application and bootloader.
   ,  #5 Separate schedule table for application and bootloader.
   ,  #6 Implement state-machine to switch between application and bootloader without disconnecting ethernet.
   ,  #7 Implement Ascii to Hex word conversion function.
   ,  #8 System variable to hold Diagnostic Session information.
   ,  #9 Change diagnostic session service handles default session, reprogramming session and extended diagnostic session.
   ,  #10 ECU reset service handles hard reset (but at present it is implemented as reset to application) and ECU shutdown.
   ,  #11 Implement ReadDataByLocalIdentifier service
   ,  #12 Implement local identifier 0xF180 - To read bootloader software version.
   ,  #13 Implement local identifier 0xF181 - To read application software version.
   ,  #14 Implement local identifier 0xF186 - To read active diagnostic session.

# 2026.04.21: branch_main_v0.0.8
Feature: #2 Introduce power-on reset timeout in bootloader.

# 2026.04.20: branch_main_v0.0.7
Feature: #1 Introduce dummy bootloader.

# 2026.04.03: branch_main_v0.0.6
Feature:
      EcuM status for shutdown request implementation 
   ,  Multi-thread implementation for ethernet rx driver
   ,  De-Initialize base software modules before initiating shutdown request.
   ,  Service-0x10-DSC
   ,  Service-0x11-EcuReset
   ,  Common response transmit logic
   ,  De-Initialize API offered to initiate shutdown sequence.

Bug-fix:
       Null pointer check for empty ring buffer pop usecase.

Known issue:
      Exit application upon shutdown request completion.

# 2026.04.02: branch_main_v0.0.5
Feature: modular development.

# 2026.03.31: branch_main_v0.0.4
Feature: Dcm seperated from core logic.

# 2026.03.27: branch_main_v0.0.3
Feature: Ring buffer introduced.

# 2026.03.25: branch_main_v0.0.2
Feature: client uses dynamic IP address to connect.

# 2026.03.06: branch_main_v0.0.1
push first version on github

