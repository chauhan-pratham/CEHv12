### Task 2: Perform Port and Service Discovery using NetScanTools Pro

#### Overview
NetScanTools Pro is a comprehensive suite of utilities designed for network professionals to gather information and troubleshoot networks. It allows for research on IPv4/IPv6 addresses, hostnames, domain names, email addresses, and URLs within the target network. In this task, we will use NetScanTools Pro to discover open ports and services running on a specified range of IP addresses.

### Steps to Perform Port and Service Discovery

1. **Install NetScanTools Pro**:
   - Navigate to `E:\CEH-Tools\CEHv12 Module 03 Scanning Networks\Scanning Tools\NetScanTools Pro` on the Windows 11 machine.
   - Double-click `nstp11demo.exe`.
   - If prompted by User Account Control, click "Yes."
   - In the Setup - NetScanTools Pro Demo window, click "Next" and follow the installation wizard steps.
   - If a WinPcap 4.1.3 Setup pop-up appears, click "Cancel."
   - In the Completing the NetScanTools Pro Demo Setup Wizard, ensure "Launch NetScanTools Pro Demo" is checked and click "Finish."

2. **Start the Demo Version**:
   - When the Reminder window appears, click the "Start the DEMO" button.
   - In the DEMO Version pop-up, click "Start NetScanTools Pro Demo…"

3. **Access the Main Window**:
   - The NetScanTools Pro main window will appear. Note that the version may differ.

4. **Ping Scanner**:
   - In the left-hand pane, scroll down to the **Manual Tools (all)** section and click on **Ping Scanner**.
   - A dialog box will open explaining the Ping Scanner tool; click "OK."
   - Ensure "Use Default System DNS" is selected.
   - Enter the range of IP addresses in the Start IP and End IP fields (e.g., `10.10.1.5 - 10.10.1.23`).
   - Click the **Start** button.
   - A Ping Scanner notice pop-up will appear; click "I Accept."

5. **View Scan Results**:
   - After the scan completes, the results will appear in your web browser (e.g., Google Chrome).
   - If prompted with "How do you want to open this file?" select Google Chrome and click "OK."
   - Close the browser and return to the NetScanTools Pro window.

6. **Port Scanner**:
   - Click the **Port Scanner** option from the left-hand pane under the Manual Tools (all) section.
   - If a dialog box appears explaining the Port Scanner tool, click "OK."
   - In the **Target Hostname or IP Address** field, enter the IP address of the target (e.g., `10.10.1.22`).
   - Ensure the **TCP Full Connect** radio button is selected.
   - Click the **Scan Range of Ports** button.
   - A Port Scanner notice pop-up will appear; click "I Accept."

7. **Analyze Port Scan Results**:
   - The results will display the active ports and their descriptions.
   - This information will help you identify active machines in the network, their respective IP addresses and hostnames, and a list of all open ports and services.

### Conclusion
- By performing the above scans, you can gather critical information that may allow for further penetration into the network, potentially leading to malicious activities such as ARP poisoning or sniffing.
- Close all open windows and document all acquired information, including screenshots and notes on discovered open ports and services. This data is essential for understanding the security posture of the target network and identifying potential vulnerabilities.