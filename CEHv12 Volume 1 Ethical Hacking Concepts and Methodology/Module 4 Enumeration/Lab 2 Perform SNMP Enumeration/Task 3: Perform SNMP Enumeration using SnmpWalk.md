#### Task 3: Perform SNMP Enumeration using SnmpWalk

1. **Access Parrot Security Machine:**
   - Log in with the default attacker username (Password: toor).

2. **Open Terminal:**
   - Gain root access by typing `sudo su`.

3. **Run SnmpWalk:**
   - Execute:
     ```
     snmpwalk -v1 -c public 10.10.1.22
     ```
   - Review the output for OIDs and associated information.

4. **Perform SNMPv2 Enumeration:**
   - Run:
     ```
     snmpwalk -v2c -c public 10.10.1.22
     ```
   - Analyze the data for user credentials and other parameters.

5. **Document Findings:**
   - Close all windows and document the acquired information.
