## Task 2: Perform Host Discovery using Angry IP Scanner

### Step-by-Step Instructions

**1. Switch to Windows 11:**
   - Click on the Windows 11 machine.

**2. Launch Angry IP Scanner:**
   - Click the Search icon on the desktop.
   - Type `angry` in the search field and open Angry IP Scanner.

**3. Follow the Getting Started Wizard:**
   - When the Getting Started window appears, click **Next** and follow the wizard until you can click **Close**.
   - If prompted with a security warning, click **Run**.

**4. Set IP Range:**
   - In the IP Range window, enter the IP range:
     ```
     10.10.1.0 to 10.10.1.255
     ```

**5. Configure Preferences:**
   - Click the Preferences icon next to the IP Range menu.
   - In the **Scanning** tab, set the Pinging method to **Combined UDP+TCP**.
   - Switch to the **Display** tab and select the **Alive hosts (responding to pings) only** option, then click **OK**.

**6. Start Scanning:**
   - Click the **Start** button to begin scanning the specified IP range.
   - Monitor the progress bar to see the scanning status.

**7. Review Scan Results:**
   - After the scan completes, a **Scan Statistics** pop-up will appear. Note the total number of alive hosts (e.g., 7) and click **Close**.
   - The results will display all active IP addresses with their hostnames in the main window.

**8. Document Findings:**
   - Close all open windows and document all the acquired information regarding the active hosts discovered.
