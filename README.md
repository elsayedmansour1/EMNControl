# EMNControl
**Embedded Multi-Network Connectivity Management System**

**Stack:** C++17, Qt 6 Framework, RESTful APIs (Qt REST Server), OpenAPI/Swagger, wpa_supplicant,
ModemManager, DBus, DHCP Client.

**•Architected** a headless Linux C++/Qt service to manage Ethernet, Wi-Fi, LTE, and hotspot interfaces, using
    
      **•wpa_supplicant** for low-level Wi-Fi control (WPA3, enterprise authentication).
  
      **•ModemManager** for LTE modem configuration (APN, PDP contexts, signal thresholds).
  
      **•hostapd** for hotspot controlling.
  
      **systemd-networkd** for ethernet controlling.
      
**•Developed** a RESTful API (Qt HTTP server) for remote network configuration and monitoring, exposing
endpoints for interface prioritization,real-time metrics (signal strength, data usage), and failover triggers.
**•Implemented unit tests** covering 85% of critical components (e.g., DHCP client logic, state machine
transitions) using Google Test, integrated into CI/CD pipelines (Jenkins) for regression testing on code
commits.
**•Developed mock interfaces** for LTE modems and Wi-Fi drivers using GMock, enabling isolated testing of
network switching logic without physical hardware.
**•Integrated code coverage** (gcov)
**•Validated** performance with packet sniffing (tcpdump).
