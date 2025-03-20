### Nmap Network Scanning Techniques Overview

1. **Launch Zenmap**: 
   - Open Zenmap on the Windows 11 machine by searching for it in the Start menu.

2. **TCP Connect Scan**:
   - Command: `nmap -sT -v 10.10.1.22`
   - Description: Performs a full TCP connect scan, completing a three-way handshake to identify open ports and services.

3. **View Scan Results**:
   - Check the **Ports/Hosts**, **Topology**, **Host Details**, and **Scans** tabs for detailed information about open ports and services.

4. **Enable Windows Firewall**:
   - On the Windows Server 2022 machine, navigate to Control Panel > System and Security > Windows Defender Firewall and enable it.

5. **Stealth Scan**:
   - Command: `nmap -sS -v 10.10.1.22`
   - Description: Performs a half-open scan, which can bypass firewall rules by not completing the TCP handshake.

6. **Xmas Scan**:
   - Command: `nmap -sX -v 10.10.1.22`
   - Description: Sends TCP frames with FIN, URG, and PUSH flags; responses indicate port status.

7. **TCP Maimon Scan**:
   - Command: `nmap -sM -v 10.10.1.22`
   - Description: Sends FIN/ACK probes; responses help determine if ports are open or closed.

8. **ACK Flag Probe Scan**:
   - Command: `nmap -sA -v 10.10.1.22`
   - Description: Sends ACK packets; no response indicates filtered ports.

9. **Disable Windows Firewall**:
   - Turn off the Windows Defender Firewall on the Windows Server 2022 machine.

10. **UDP Scan**:
    - Command: `nmap -sU -v 10.10.1.22`
    - Description: Scans for open UDP ports; no response indicates open ports.

11. **Create a Null Scan Profile**:
    - In Zenmap, create a new profile for a Null Scan (`-sN`) with aggressive options enabled.

12. **Scan Ubuntu Machine**:
    - Command: Use the Null Scan profile on target IP `10.10.1.9`.

13. **Additional Scanning Techniques**:
    - **IDLE Scan**: `nmap -sI -v [target IP]`
    - **SCTP INIT Scan**: `nmap -sY -v [target IP]`
    - **SCTP COOKIE ECHO Scan**: `nmap -sZ -v [target IP]`

14. **Service Version Detection**:
    - Command: `nmap -sV 10.10.1.22`
    - Description: Detects service versions running on open ports.

15. **Aggressive Scan**:
    - Command: `nmap -A 10.10.1.*`
    - Description: Scans the entire subnet for OS, version, and service details.

16. **Review Host Details**:
    - Select an IP from the scan results to view detailed information about the host.

### Conclusion
This guide summarizes the steps to discover open ports, services, and their versions on target networks using various Nmap scanning techniques. Document all acquired information for future reference.