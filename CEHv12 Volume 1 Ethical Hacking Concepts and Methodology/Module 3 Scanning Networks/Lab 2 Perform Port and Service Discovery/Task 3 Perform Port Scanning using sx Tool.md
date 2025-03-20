### Task 3: Perform Port Scanning using sx Tool

#### Overview
The `sx` tool is a command-line network scanner that can perform various types of scans, including ARP scans, ICMP scans, TCP SYN scans, UDP scans, and application-specific scans. In this task, we will use `sx` to perform ARP scans, TCP scans, and UDP scans to discover open ports on a target machine.

### Steps to Perform Port Scanning using sx Tool

1. **Switch to Parrot Security Machine**:
   - Click on **Parrot Security** to access the machine.

2. **Log In**:
   - The attacker username will be selected by default. Enter the password `toor` in the Password field and press Enter.
   - If a Parrot Updater pop-up appears, ignore and close it.
   - If a question pop-up window appears asking to update the machine, click "No" to close the window.

3. **Open Terminal**:
   - Click the **MATE Terminal** icon at the top of the Desktop to open a terminal window.

4. **Gain Root Access**:
   - In the terminal window, type `sudo su` and press Enter.
   - Enter the password `toor` when prompted (the password will not be visible).

5. **Perform ARP Scan**:
   - Type `sx arp 10.10.1.0/24` and press Enter to scan all IP addresses and MAC addresses associated with connected devices in the local network.
   - This command performs an ARP scan.

6. **Create ARP Cache File**:
   - Type `sx arp 10.10.1.0/24 --json | tee arp.cache` and press Enter.
   - This command creates an `arp.cache` file in JSON format, which will be used for subsequent scans.

7. **Perform TCP Scan**:
   - Type `cat arp.cache | sx tcp -p 1-65535 10.10.1.11` and press Enter to list all open TCP ports on the target machine (replace `10.10.1.11` with the actual target IP address).
   - This command performs a TCP scan on the specified range of ports (1-65535).

8. **View Help Commands**:
   - Type `sx help` and press Enter to obtain a list of commands that can be used with `sx`.
   - For more detailed information, you can use `sx --help`.

9. **Perform UDP Scan**:
   - To check if a specific port is open or closed, type `cat arp.cache | sx udp --json -p 53 10.10.1.11` and press Enter (replace `10.10.1.11` with the actual target IP address).
   - This command performs a UDP scan on port 53.
   - The result will indicate whether the port is open or closed based on the reply packet received.

10. **Check Another UDP Port**:
    - Type `cat arp.cache | sx udp --json -p 500 10.10.1.11` and press Enter (replace `10.10.1.11` with the actual target IP address).
    - If there is no reply code, it indicates that the target port is open.

### Conclusion
- This concludes the demonstration of port scanning using the `sx` tool. You have successfully performed ARP scans, TCP scans, and UDP scans to discover open ports on the target machine.
- Close all open windows and document all acquired information, including screenshots and notes on discovered open ports and services. This information is vital for assessing the security posture of the target network and identifying potential vulnerabilities.