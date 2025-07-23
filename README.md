# Embedded Multi-Network Connectivity Management System

**Stack**: C++17, Qt 5.15 Framework, RESTful APIs (Qt REST Server), OpenAPI/Swagger, nginx, wpa_supplicant, ModemManager, DBus, DHCP Client

- **Developed C++/Qt Service**  
  Managed Ethernet, Wi-Fi, LTE, and hotspot interfaces using:  
  - `wpa_supplicant` for low-level Wi-Fi control (WPAS, enterprise authentication)  
  - `ModemManager` for LTE modem configuration (APN, PDP contexts, signal thresholds)  
  - `hostapd` for hotspot controlling  

- **Developed RESTful API**  
  Built Qt HTTP server for remote network configuration/monitoring, exposing endpoints for:  
  - Interface prioritization  
  - Real-time metrics (signal strength, data usage)  
  - Failover triggers  

- **Developed Web Configuration Interface**  
  Nginx-based service consuming REST API to provide user-facing web UI  

- **Developed Unit Tests**  
  Covered 85% of critical components (e.g., DHCP client logic, state machine transitions) using Google Test  
  Integrated into CI/CD pipelines (Jenkins) for regression testing on code commits  

- **Developed Mock Interfaces**  
  Simulated LTE modems/Wi-Fi drivers using GMock for isolated testing of network switching logic  

- **Integrated Code Coverage**  
  Implemented `gcov` for test coverage analysis  

- **Performance Validation**  
  Conducted packet sniffing validation via `tcpdump`