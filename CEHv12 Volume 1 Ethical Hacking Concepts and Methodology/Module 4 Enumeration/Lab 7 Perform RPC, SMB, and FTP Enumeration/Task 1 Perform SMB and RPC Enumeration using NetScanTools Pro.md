**Objective:** Extract detailed information about systems in the target network using various enumeration techniques.

#### Task 1: Perform SMB and RPC Enumeration using NetScanTools Pro

1. **Setup NetScanTools Pro:**
   - Log in to Windows Server 2019 (Password: Pa$$w0rd).
   - Install NetScanTools Pro from the specified directory.
   - Launch NetScanTools Pro and navigate to the SMB Scanner.

2. **Configure SMB Scanner:**
   - Add target IP addresses (10.10.1.19 and 10.10.1.22) to the target list.
   - Enter login credentials (Username: Administrator, Password: Pa$$w0rd).
   - Click "Get SMB Versions" to scan for SMB services.

3. **View SMB Shares:**
   - Right-click on the target IP (10.10.1.19) and select "View Shares" to see shared files and permissions.

4. **Perform RPC Enumeration:**
   - Navigate to the *nix RPC Info tool.
   - Enter the target IP (10.10.1.19) and click "Dump Portmap" to view RPC info.