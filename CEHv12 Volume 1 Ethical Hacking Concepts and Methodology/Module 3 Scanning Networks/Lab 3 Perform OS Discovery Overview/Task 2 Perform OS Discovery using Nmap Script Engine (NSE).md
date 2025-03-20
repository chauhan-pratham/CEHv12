### Task 2: Perform OS Discovery using Nmap Script Engine (NSE)

1. **Switch to Parrot Security**:
   - Log in with username `attacker` and password `toor`.

2. **Open Terminal**:
   - Launch the MATE Terminal.

3. **Switch to Root User**:
   - Run: `sudo su` and enter the password `toor`.

4. **Aggressive Scan**:
   - Command: `nmap -A 10.10.1.22`
   - Description: Performs an aggressive scan to identify OS and services.

5. **OS Discovery**:
   - Command: `nmap -O 10.10.1.22`
   - Description: Specifically performs OS discovery.

6. **SMB OS Discovery**:
   - Command: `nmap --script smb-os-discovery.nse 10.10.1.22`
   - Description: Uses SMB protocol to gather OS and system information.