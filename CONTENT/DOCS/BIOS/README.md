## BIOS Configuration
1. **Start FRESH**
   - Reset BIOS to optimal defaults, may have to search on how to reset.
2. **Set the Package C-State Limit**
   - When higher C-States values are made available such as  C6, C7, C8 the more latency is introduced due to the time it takes to restore and transition the active power state.
   - Some configurations may be negatively impacted by disabling all avaiable C-States, if this is the case then try limiting the value to **C2 or C3**. This is likely due to a bottleneck in memory or cpu.
3. **Disable Intel (R) Speed Shift Technology & Intel(R) SpeedStep Technology (EIST) Function**
4. **Turbo Boost**
   - If isolating performance behavior issues, disable.
   - If you'd like to use Turbo Boost frequencies I'd recommend using a static overclock to reduce minor overhead from dynamic frequency scaling, otherwise **enable**.
5. **Enable XMP Profile**
6. Set any **Fast Boot Settings to OFF**
   - This can increase latency. Disable if it affects USB port connectivity.
7. **Disable any Active State Power Management (ASPM)/Aggressive Link Power Management (ALPM) settings**
   - This may be in the SATA and/or PCI configuration sections, check each section
8. Set your **SATA disk controlled mode to AHCI**
9. Disable OnBoard Video, Audio or Lan Controller if you have a PCI/USB one that is or will be installed.
10. Set your **Primary Display Output to your dedicated graphics** card if present
11. Leave High Precision Event Timer (HPET) ON in the BIOS if present or if it is enabled by default
12. **Disable any onboard LED/RGB traces/lights**
   - May use CPU resources and increase latency.
13. Set your **PCI Express Max Link Speed to Gen3**, devices can negotiate lower spec as needed.

### Other Considerations
* Disable or Enable Legacy USB Support & Port 60/64 Emulation
    - Having them enabled **may** cause the CPU to enter System Management Mode (SMM) via System Management Interrupt (SMI) which is a non blocking interrupt and may introduce minor latency.
    - If you're setting up a non UEFI operating system this may need to be on during install and can be turned off afterwards.
    - Your mileage may vary on this configuration option, typically the default is Legacy USB Support enabled. Try it and see if it negatively impacts your perceived user experience.
