### Summary of Steps for Detecting Session Hijacking using Wireshark

#### Lab Scenario Overview
Session hijacking poses significant risks, including identity theft and loss of sensitive information. This lab demonstrates how to detect session hijacking attacks using Wireshark, a powerful packet analysis tool.

### Task 1: Detect Session Hijacking using Wireshark

1. **Prepare the Environment:**
   - Use the Parrot Security machine (IP: 10.10.1.13) to perform a session hijacking attack on the Windows 11 machine (IP: 10.10.1.11).

2. **Launch Wireshark on Windows 11:**
   - Switch to the Windows 11 machine.
   - Click the Search icon on the Desktop, type "wire," and select Wireshark from the results to open it.
   - In the Wireshark window, double-click the primary network interface (e.g., Ethernet) to start capturing network traffic.

3. **Start Capturing Traffic:**
   - Leave Wireshark running to capture live network traffic.

4. **Perform Session Hijacking Attack using bettercap:**
   - Switch to the Parrot Security machine.
   - Open a Terminal window by clicking the MATE Terminal icon.
   - Gain root access by typing:
     ```bash
     sudo su
     ```
   - Enter the password `toor` when prompted.

5. **Set Up bettercap:**
   - Change to the root directory:
     ```bash
     cd
     ```
   - Start bettercap with the specified network interface:
     ```bash
     bettercap -iface eth0
     ```
   - Enable network probing:
     ```bash
     net.probe on
     ```
   - Start the network reconnaissance module:
     ```bash
     net.recon on
     ```
   - Begin sniffing network traffic:
     ```bash
     net.sniff on
     ```

6. **Monitor ARP Packets in Wireshark:**
   - Switch back to the Windows 11 machine and observe the captured packets in Wireshark.
   - Look for a high number of ARP packets, which indicate that the attacker’s machine (10.10.1.13) is acting as a client for all IP addresses in the subnet.
   - This behavior suggests that packets from the victim node (10.10.1.11) are being routed through the attacker’s machine, a sign of a potential session hijacking attack.

7. **Conclusion:**
   - This demonstration shows how to detect session hijacking attacks using Wireshark by monitoring network traffic and identifying unusual ARP activity.
   - Close all open windows and document all acquired information regarding the detected session hijacking attempt.

This summary outlines the essential steps for detecting session hijacking using Wireshark, emphasizing the importance of monitoring network traffic for security professionals.