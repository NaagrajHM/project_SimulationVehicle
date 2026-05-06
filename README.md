# project_SimulationVehicle
Repository for Vehicle Simulation.

# 2026.05.05:
      #19 2026.05.05: branch_main_v0.0.11 - FEATURE - Implement (a dummy) request download service.
   ,  #20 2026.05.05: branch_main_v0.0.11 - BUGFIX - Unknown service request send negative response code - service not supported.
   ,  #21 2026.05.05: branch_main_v0.0.11 - BUGFIX - Unknown sub-function request send negative response code - sub-function not supported - Diagnostic session change.
   ,  #22 2026.05.05: branch_main_v0.0.11 - BUGFIX - Unknown sub-function request send negative response code - sub-function not supported - ECU Reset.
   ,  #23 2026.05.05: branch_main_v0.0.11 - BUGFIX - Unknown sub-function request send negative response code - sub-function not supported - Security access.
   ,  #24 2026.05.05: branch_main_v0.0.11 - BUGFIX - Unknown sub-function request send negative response code - sub-function not supported - Tester present.
   ,  #25 2026.05.05: branch_main_v0.0.11 - BUGFIX - Unknown local identifier request send negative response code - sub-function not supported - Read data by local identifier.
   ,  #26 2026.05.05: branch_main_v0.0.11 - BUGFIX - Diagnostic session change to re-programming is allowed only through extended session.
   ,  #27 2026.05.05: branch_main_v0.0.11 - BUGFIX - Diagnostic session change from re-programming to default must go through reset-to-application.
   ,  #28 2026.05.05: branch_main_v0.0.11 - BUGFIX - Read bootloader version request when in application mode send negative response code - request out of range.
   ,  #29 2026.05.05: branch_main_v0.0.11 - BUGFIX - Read application version request when in bootloader mode send negative response code - request out of range.
   ,  #30 2026.05.05: branch_main_v0.0.11 - BUGFIX - Upgrade diagnostic session change logic with ServicesSystemEcuM_geModeCurrent in consideration.
   ,  #31 2026.05.05: branch_main_v0.0.11 - BUGFIX - not implemented - suppress positive response - Tester present.

# 2026.04.27: branch_main_v0.0.10
Feature:
      #15 Type define uint32.
   ,  #16 Implement ASCII to DWORD(uint32) conversion.
   ,  #17 Implement SecurityAccess service and required infrastructure.

Known issue:
   ,  #18 Optimize ASCII to HEX conversions.

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

