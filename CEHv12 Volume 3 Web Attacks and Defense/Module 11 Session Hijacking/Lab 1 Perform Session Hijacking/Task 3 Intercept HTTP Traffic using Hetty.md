### Summary of Steps for Intercepting HTTP Traffic using Hetty

#### Lab Scenario Overview
In this task, we will use Hetty, an HTTP toolkit, to intercept HTTP traffic between a target machine (Windows Server 2022) and an attacker machine (Windows 11). Hetty allows for manual request editing and replaying, making it a powerful tool for security research.

### Task 3: Intercept HTTP Traffic using Hetty

1. **Launch Hetty on Attacker Machine (Windows 11):**
   - Switch to the Windows 11 machine.
   - Navigate to `E:\CEH-Tools\CEHv12 Module 11 Session Hijacking\Hetty` and double-click `hetty.exe`.
   - Click "Run" on the Security Warning prompt.
   - Wait for the Command Prompt window to initialize Hetty.

2. **Access Hetty Dashboard:**
   - Minimize all windows and open a web browser (e.g., Mozilla Firefox).
   - In the address bar, type `http://localhost:8080` and press Enter to open the Hetty dashboard.

3. **Create a New Project:**
   - Click the "MANAGE PROJECTS" button.
   - Under the New Project section, enter the project name as "Moviescope" and click "+ CREATE & OPEN PROJECT".
   - Confirm that the "Moviescope" project is now active.

4. **View Proxy Logs:**
   - Click on the Proxy logs icon in the left pane to access the logs.

5. **Configure Proxy on Target Machine (Windows Server 2022):**
   - Switch to the Windows Server 2022 machine and log in using the password `Pa$$w0rd`.
   - Open Google Chrome and navigate to Settings > System > Open your computer’s proxy settings.
   - Enable the proxy server with the following settings:
     - Address: `10.10.1.11` (IP of Windows 11)
     - Port: `8080`
   - Save the settings and close the browser.

6. **Access Target Website:**
   - In the Chrome browser on Windows Server 2022, open a new tab and navigate to `http://www.moviescope.com`.

7. **Capture Logs in Hetty:**
   - Switch back to the Windows 11 machine and observe the captured logs in the Proxy logs page, focusing on entries related to `moviescope.com`.

8. **Log in as Victim:**
   - On the Windows Server 2022 machine, log in to the MovieScope website using the credentials `sam/test`.

9. **Review Captured Credentials:**
   - Return to the Windows 11 machine and scroll through the Proxy logs to find the POST request associated with the MovieScope login.
   - Select the POST request and view the Body tab to see the captured user credentials.

10. **Reset Proxy Settings:**
    - Switch back to the Windows Server 2022 machine and revert the proxy settings to default by disabling the proxy server.

11. **Conclusion:**
    - Close all open windows and document all acquired information regarding the intercepted traffic and credentials.

This summary outlines the essential steps for intercepting HTTP traffic using Hetty, demonstrating the process of capturing and analyzing web traffic for security research purposes.