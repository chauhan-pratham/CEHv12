#### Task 2: Perform RPC, SMB, and FTP Enumeration using Nmap

1. **Setup FTP Service:**
   - Log in to Windows Server 2019 and create an FTP site named "CEH.com" with the physical path set to "C:\FTP-Site Data."
   - Configure the FTP site to allow all users with read and write permissions.

2. **Nmap Enumeration:**
   - Open a terminal in Parrot Security and gain root access: `sudo su` (Password: toor).
   - Check FTP service: `nmap -p 21 10.10.1.19` to confirm port 21 is open.
   - Perform an aggressive scan: `nmap -T4 -A 10.10.1.19` to gather detailed information about open ports and services.

3. **Scan Specific Ports:**
   - For SMB: `nmap -p 445 -A 10.10.1.19`.
   - For FTP: `nmap -p 21 -A 10.10.1.19`.

---

This summary captures the key steps and commands for performing RPC, SMB, and FTP enumeration effectively. Let me know if you need any further modifications or additional information!