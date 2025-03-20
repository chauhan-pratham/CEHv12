### Summary of Steps to Perform Network Scanning Using Metasploit

1. **Prepare Environment:**
   - Switch to the Parrot Security machine and open a terminal.
   - Gain root access by typing `sudo su` (password: toor).

2. **Start PostgreSQL Service:**
   - Run the command: 
     ```
     service postgresql start
     ```

3. **Launch Metasploit:**
   - Start Metasploit with:
     ```
     msfconsole
     ```
   - Check database connection with:
     ```
     db_status
     ```
   - If not connected, initialize the database with:
     ```
     msfdb init
     ```
   - Restart PostgreSQL and relaunch Metasploit.

4. **Scan Target Network:**
   - Execute the Nmap command to scan the subnet:
     ```
     nmap -Pn -sS -A -oX Test 10.10.1.0/24
     ```
   - Import the scan results into Metasploit:
     ```
     db_import Test
     ```

5. **View Active Hosts and Services:**
   - List active hosts:
     ```
     hosts
     ```
   - List running services:
     ```
     services
     ```

6. **Perform SYN Scan:**
   - Use the SYN scan module:
     ```
     use auxiliary/scanner/portscan/syn
     ```
   - Set parameters:
     ```
     set INTERFACE eth0
     set PORTS 80
     set RHOSTS 10.10.1.5-23
     set THREADS 50
     ```
   - Run the scan:
     ```
     run
     ```

7. **Perform TCP Scan:**
   - Load the TCP scan module:
     ```
     use auxiliary/scanner/portscan/tcp
     ```
   - Set target IP or use discovered hosts:
     ```
     set RHOSTS 10.10.1.22
     ```
   - Run the scan to discover open TCP ports.

8. **Determine OS Versions:**
   - Use the SMB version scanner:
     ```
     use auxiliary/scanner/smb/smb_version
     ```
   - Set parameters:
     ```
     set RHOSTS 10.10.1.5-23
     set THREADS 11
     ```
   - Run the scan to identify OS details.

9. **Explore Further:**
   - Investigate other Metasploit modules (e.g., FTP) for additional information.

10. **Documentation:**
    - Close all windows and document the findings from the scans.

This summary outlines the essential steps for using Metasploit to scan a target network, identify active hosts, open ports, and gather OS information.