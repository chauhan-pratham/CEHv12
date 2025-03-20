## Task 1: Perform Host Discovery using Nmap

### Step-by-Step Instructions

**1. Switch to Parrot Security:**
   - Select the Parrot Security machine.
   - Log in with the username (default) and enter the password `toor`.

**2. Open Terminal:**
   - Click the MATE Terminal icon on the desktop to open a terminal window.

**3. Gain Root Access:**
   - In the terminal, type:
     ```bash
     sudo su
     ```
   - Enter the password `toor` when prompted.

**4. Perform ARP Ping Scan:**
   - Type the following command to perform an ARP ping scan on the target IP address (e.g., `10.10.1.22`):
     ```bash
     nmap -sn -PR 10.10.1.22
     ```
   - This command will show if the target host is up.

**5. Perform UDP Ping Scan:**
   - Next, perform a UDP ping scan:
     ```bash
     nmap -sn -PU 10.10.1.22
     ```
   - This will send UDP packets to the target host and check for responses.

**6. Perform ICMP ECHO Ping Scan:**
   - Now, perform an ICMP ECHO ping scan:
     ```bash
     nmap -sn -PE 10.10.1.22
     ```
   - This sends ICMP ECHO requests to the host.

**7. Perform ICMP ECHO Ping Sweep:**
   - To discover live hosts in a range, use:
     ```bash
     nmap -sn -PE 10.10.1.10-23
     ```
   - This will scan the specified range for active hosts.

**8. Perform ICMP Timestamp Ping Scan:**
   - Execute the following command:
     ```bash
     nmap -sn -PP 10.10.1.22
     ```
   - This performs an ICMP timestamp ping scan.

**9. Additional Scanning Techniques:**
   - You can also use the following commands for different scanning techniques:
     - ICMP Address Mask Ping Scan:
       ```bash
       nmap -sn -PM 10.10.1.22
       ```
     - TCP SYN Ping Scan:
       ```bash
       nmap -sn -PS 10.10.1.22
       ```
     - TCP ACK Ping Scan:
       ```bash
       nmap -sn -PA 10.10.1.22
       ```
     - IP Protocol Ping Scan:
       ```bash
       nmap -sn -PO 10.10.1.22
       ```

**10. Document Findings:**
   - Close all open windows and document all the acquired information regarding the live hosts discovered.
