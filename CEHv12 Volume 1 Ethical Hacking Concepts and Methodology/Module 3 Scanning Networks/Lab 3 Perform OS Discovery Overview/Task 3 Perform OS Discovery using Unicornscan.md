### Task 3: Perform OS Discovery using Unicornscan

1. **Open Terminal**:
   - Launch the MATE Terminal in Parrot Security.

2. **Switch to Root User**:
   - Run: `sudo su` and enter the password `toor`.

3. **Immediate Mode Scan**:
   - Command: `unicornscan 10.10.1.22 -Iv`
   - Description: Scans the target machine and displays open TCP ports and TTL values.

4. **Analyze Results**:
   - TTL value of 128 indicates a Windows OS.
   - Command: `unicornscan 10.10.1.9 -Iv` for the Ubuntu machine.
   - TTL value of 64 indicates a Linux-based OS.

### Conclusion
This lab demonstrated various methods for OS discovery using Wireshark, Nmap, and Unicornscan. Document all findings for future reference and analysis.