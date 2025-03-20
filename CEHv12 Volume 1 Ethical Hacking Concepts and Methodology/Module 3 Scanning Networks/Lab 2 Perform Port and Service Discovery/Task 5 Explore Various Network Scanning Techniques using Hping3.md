### Hping3 Network Scanning Techniques Overview

1. **Launch Parrot Security**:
   - Log in with username `attacker` and password `toor`.
   - Close any update pop-ups.

2. **Open Terminal**:
   - Click the MATE Terminal icon to open a terminal window.

3. **Switch to Root User**:
   - Command: `sudo su`
   - Enter password `toor` when prompted.

4. **Navigate to Root Directory**:
   - Command: `cd`

5. **ACK Scan**:
   - Command: `hping3 -A 10.10.1.22 -p 80 -c 5`
   - Description: Sends ACK packets to port 80. If packets sent and received are equal, the port is open.

6. **SYN Scan**:
   - Command: `hping3 -8 0-100 -S 10.10.1.22 -V`
   - Description: Scans ports 0-100 using SYN packets. Displays open ports and associated services.

7. **FIN, PUSH, and URG Scan**:
   - Command: `hping3 -F -P -U 10.10.1.22 -p 80 -c 5`
   - Description: Sends packets with FIN, PUSH, and URG flags to port 80. Equal packets sent and received indicate the port is open.

8. **TCP Stealth Scan**:
   - Command: `hping3 --scan 0-100 -S 10.10.1.22`
   - Description: Scans ports 0-100 with SYN packets. A SYN+ACK response indicates open ports.

9. **ICMP Scan**:
   - Command: `hping3 -1 10.10.1.22 -p 80 -c 5`
   - Description: Sends ICMP echo requests to port 80. Responses confirm the host is up.

10. **Additional Scanning Techniques**:
    - **Subnet Scan**: `hping3 -1 [Target Subnet] --rand-dest -I eth0`
    - **UDP Scan**: `hping3 -2 10.10.1.22 -p 80 -c 5`

### Conclusion
This guide summarizes the steps to discover open ports and services on target networks using various Hping3 scanning techniques. Document all acquired information for future reference.