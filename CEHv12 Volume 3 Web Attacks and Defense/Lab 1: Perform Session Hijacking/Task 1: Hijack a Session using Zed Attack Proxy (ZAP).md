### Summary of Steps for Performing Session Hijacking

#### Lab Scenario Overview
Session hijacking allows an attacker to take over an active session by stealing or guessing a valid session ID. This lab demonstrates how to hijack a session using various tools, including Zed Attack Proxy (ZAP) and bettercap.

### Task 1: Hijack a Session using Zed Attack Proxy (ZAP)

1. **Configure Proxy on Victim Machine (Windows 11):**
   - Log in to the Windows 11 machine using the password `Pa$$w0rd`.
   - Open Google Chrome and navigate to Settings > System > Open your computer’s proxy settings.
   - Enable the proxy server with IP `10.10.1.19` and Port `8080`, then save.

2. **Launch ZAP on Attacker Machine (Windows Server 2019):**
   - Log in to the Windows Server 2019 machine using the password `Pa$$w0rd`.
   - Search for and launch ZAP.
   - Choose not to persist the session and click Start.

3. **Set Up ZAP:**
   - Click the “+” icon and select Break to enable request/response modification.
   - Go to Options > Local Proxies and set the Address to `10.10.1.19` and Port to `8080`.
   - Enable global breakpoints by clicking the Set break on all requests and responses icon.

4. **Intercept Traffic:**
   - Switch back to the Windows 11 machine and open Chrome.
   - Navigate to `www.moviescope.com`, click Advanced, and proceed to the site.
   - Return to ZAP and capture the requests in the Break tab.

5. **Modify Requests:**
   - Change all captured GET requests from `www.moviescope.com` to `www.goodshopping.com`.
   - Submit each modified request to forward the traffic to the victim’s machine.

6. **Verify Changes:**
   - On the Windows 11 machine, confirm that the browser displays `www.goodshopping.com` while the address bar shows `www.moviescope.com`.

7. **Reset Proxy Settings:**
   - Revert the proxy settings on the Windows 11 machine to default by disabling the proxy server.