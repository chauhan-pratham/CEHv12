#### Task 3: Perform NetBIOS Enumeration using an NSE Script

1. **Access Parrot Security Machine:**
   - Log in with the default attacker username (Password: toor).

2. **Open Terminal:**
   - Type `sudo su` to gain root access.

3. **Run NSE Script:**
   - Execute the command:
     ```
     nmap -sV -v --script nbstat.nse 10.10.1.22
     ```
   - This retrieves NetBIOS names and MAC addresses.

4. **Perform UDP Scan:**
   - Run:
     ```
     nmap -sU -p 137 --script nbstat.nse 10.10.1.22
     ```
   - This scans for the NetBIOS service on UDP port 137.

5. **Document Findings:**
   - Close all windows and document the acquired information.

---

### Conclusion
This summary outlines the essential steps for performing NetBIOS enumeration using various methods, including Windows command-line utilities, the NetBIOS Enumerator tool, and NSE scripts. Each task provides a different approach to gather information about the target network, which can be useful for further penetration testing and vulnerability assessment.