#### Task 1: Perform NetBIOS Enumeration using Windows Command-Line Utilities

1. **Access Windows Server 2019:**
   - Log in using the Administrator account (Password: Pa$$w0rd).

2. **Open Command Prompt:**
   - Type `nbtstat -a 10.10.1.11` to display the NetBIOS name table of the target Windows 11 machine.

3. **List NetBIOS Name Cache:**
   - Run `nbtstat -c` to view the NetBIOS name cache.

4. **Check Network Connections:**
   - Execute `net use` to display information about shared resources and connections.

5. **Document Findings:**
   - Close all windows and document the acquired information.
