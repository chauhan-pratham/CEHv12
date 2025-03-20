#### Task 1: Perform NFS Enumeration using RPCScan and SuperEnum

1. **Enable NFS Service on Windows Server 2019:**
   - Log in to Windows Server 2019 (Password: Pa$$w0rd).
   - Open Server Manager and navigate to "Add roles and features."
   - Select "Server for NFS" under "File and Storage Services" and install it.
   - Close the installation wizard once completed.

2. **Check NFS Service Status:**
   - Switch to Parrot Security and open a terminal.
   - Gain root access: `sudo su` (Password: toor).
   - Run `nmap -p 2049 10.10.1.19` to verify that port 2049 (NFS) is open.

3. **Use SuperEnum for NFS Enumeration:**
   - Navigate to the SuperEnum directory: `cd SuperEnum`.
   - Create a target file: `echo "10.10.1.19" >> Target.txt`.
   - Run SuperEnum: `./superenum`, inputting `Target.txt` when prompted.
     - If you encounter an error, run `chmod +x superenum` and try again.
   - Wait for the scan (15-20 mins) and review results for open ports and NFS service.

4. **Use RPCScan for NFS Enumeration:**
   - Navigate to the RPCScan directory: `cd RPCScan`.
   - Execute the RPCScan script: `python3 rpc-scan.py 10.10.1.19 --rpc`.
   - Review results to confirm that port 2049 is open and NFS is running.

---

This summary captures the key steps and commands for performing NFS enumeration effectively. Let me know if you need any further modifications or additional information!