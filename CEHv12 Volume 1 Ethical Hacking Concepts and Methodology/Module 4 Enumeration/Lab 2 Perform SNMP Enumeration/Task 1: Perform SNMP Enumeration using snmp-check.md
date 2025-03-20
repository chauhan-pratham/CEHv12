#### Task 1: Perform SNMP Enumeration using snmp-check

1. **Access Parrot Security Machine:**
   - Log in with the default attacker username (Password: toor).

2. **Open Terminal:**
   - Gain root access by typing `sudo su`.

3. **Check SNMP Port:**
   - Run the command:
     ```
     nmap -sU -p 161 10.10.1.22
     ```
   - Confirm that port 161 is open.

4. **Perform SNMP Enumeration:**
   - Execute:
     ```
     snmp-check 10.10.1.22
     ```
   - Review the output for system information, user accounts, network details, and more.

5. **Document Findings:**
   - Close all windows and document the acquired information.

---