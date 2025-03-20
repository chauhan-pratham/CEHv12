### Task 1: Perform Port and Service Discovery using MegaPing

1. **Install MegaPing**:
   - Navigate to `E:\CEH-Tools\CEHv12 Module 03 Scanning Networks\Scanning Tools\MegaPing` on the Windows 11 machine.
   - Double-click `megaping_setup.exe`.
   - If prompted by User Account Control, click "Yes."
   - Follow the installation wizard steps and click "Finish" after installation.
   - Check the "Launch the program" checkbox to open MegaPing.

2. **Agree to Terms**:
   - In the "About MegaPing" window, click the "I Agree" button.

3. **Open IP Scanner**:
   - In the MegaPing GUI, select the **IP Scanner** option from the left pane.
   - In the IP Scanner tab, enter the IP range:
     - **From**: `10.10.1.5`
     - **To**: `10.10.1.20`
   - Click the **Start** button.

4. **View Results**:
   - MegaPing will list all IP addresses in the specified range, showing their TTL values, status (dead or alive), and statistics for dead and alive hosts.

5. **Open Port Scanner**:
   - Select the **Port Scanner** option from the left pane.
   - In the Port Scanner tab, enter the IP address of the target machine (e.g., `10.10.1.22` for Windows Server 2022) into the **Destination Address List** field and click **Add**.

6. **Start Port Scanning**:
   - Check the box next to `10.10.1.22` and click the **Start** button to begin scanning for open ports on that machine.

7. **Analyze Port Information**:
   - MegaPing will display the ports associated with the Windows Server 2022 (10.10.1.22), including:
     - Port number and type
     - Services running on each port
     - Descriptions and associated risks
   - This information can help identify potential vulnerabilities in the target network.

8. **Repeat Scanning**:
   - You can perform similar port and service scanning on other target machines as needed.

### Conclusion
- Close all open windows and document all acquired information, including screenshots and notes on discovered open ports and services. This information is crucial for understanding the security posture of the target network and identifying potential attack vectors.