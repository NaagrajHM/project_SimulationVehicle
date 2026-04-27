# project_SimulationVehicle
Repository for Vehicle Simulation.

# 2026.04.27: Use-case scenario for Request download 
0.500000 1  7E0             Rx   d 8 02 10 03 00 00 00 00 00  // Tester: Switch to Extended Session
0.504200 1  7E8             Rx   d 8 06 50 03 00 32 01 F4 AA  // ECU: Positive Response
0.650000 1  7E0             Rx   d 8 02 27 01 00 00 00 00 00  // Tester: Security Access (Request Seed)
0.652100 1  7E8             Rx   d 8 06 67 01 11 22 33 44 AA  // ECU: Seed (0x11223344)
0.700000 1  7E0             Rx   d 8 06 27 02 AA BB CC DD 00  // Tester: Send Key (Dummy)
0.703500 1  7E8             Rx   d 8 02 67 02 00 00 00 00 00  // ECU: Security Access Granted
0.850000 1  7E0             Rx   d 8 02 10 02 00 00 00 00 00  // Tester: Switch to Programming Session
0.858000 1  7E8             Rx   d 8 06 50 02 00 32 01 F4 AA  // ECU: Response (Now in Bootloader)
1.000000 1  7E0             Rx   d 8 07 34 00 44 00 40 00 00  // Tester: Request Download
1.000001 1  7E0             Rx   d 8 10 00 00 00 00 00 00 00  // (Address 0x400000, Size 0x1000)
1.005000 1  7E8             Rx   d 8 04 74 20 04 02 00 00 00  // ECU: Acknowledged (Max Block Length 0x402)

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

