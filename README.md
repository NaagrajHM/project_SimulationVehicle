# project_SimulationVehicle
Repository for Vehicle Simulation.

# 2026.04.20: branch_main_v0.0.7
Feature: Introduce dummy bootloader.

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

