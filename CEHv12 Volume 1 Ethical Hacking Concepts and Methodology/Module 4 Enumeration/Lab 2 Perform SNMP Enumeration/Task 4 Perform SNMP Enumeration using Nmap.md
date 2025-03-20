#### Task 4: Perform SNMP Enumeration using Nmap

1. **Access Parrot Security Machine:**
   - Log in with the default attacker username (Password: toor).

2. **Open Terminal:**
   - Gain root access by typing `sudo su`.

3. **Run Nmap SNMP Scripts:**
   - Execute the following commands to gather information:
     - For system description:
       ```
       nmap -sU -p 161 --script=snmp-sysdescr 10.10.1.22
       ```
     - For running processes:
       ```
       nmap -sU -p 161 --script=snmp-processes 10.10.1.22
       ```
     - For installed software:
       ```
       nmap -sU -p 161 --script=snmp-win32-software 10.10.1.22
       ```
     - For network interfaces:
       ```
       nmap -sU -p 161 --script=snmp-interfaces 10.10.1.22
       ```

4. **Review Results:**
   - Analyze the output for details about the SNMP server, running processes, installed applications, and network interfaces.

5. **Document Findings:**
   - Close all windows and document the acquired information.

---

### Conclusion
This summary outlines the essential steps for performing SNMP enumeration using various methods, including `snmp-check`, SoftPerfect Network Scanner, SnmpWalk, and Nmap. Each task provides a different approach to gather information about the target network, which can be useful for further penetration testing and vulnerability assessment.