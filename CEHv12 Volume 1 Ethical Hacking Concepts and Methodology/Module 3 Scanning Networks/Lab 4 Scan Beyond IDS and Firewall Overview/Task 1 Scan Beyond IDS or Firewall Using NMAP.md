1. **Enable Windows Firewall**:
   - On the Windows 11 machine, navigate to Control Panel > System and Security > Windows Defender Firewall and enable it.

2. **Launch Wireshark**:
   - Open Wireshark and start capturing packets on the Ethernet interface.

3. **Switch to Parrot Security**:
   - Open the MATE Terminal and switch to root user: `sudo su` (password: `toor`).

4. **Packet Fragmentation**:
   - Command: `nmap -f 10.10.1.11`
   - Description: Splits packets into smaller fragments to evade detection by the firewall.

5. **Observe Fragmented Packets**:
   - Check Wireshark for captured fragmented packets.

6. **Source Port Manipulation**:
   - Command: `nmap -g 80 10.10.1.11`
   - Description: Uses port 80 to manipulate source port and evade IDS/firewall.

7. **MTU Manipulation**:
   - Command: `nmap -mtu 8 10.10.1.11`
   - Description: Sends smaller packets (8 bytes) to bypass filtering.

8. **IP Address Decoy**:
   - Command: `nmap -D RND:10 10.10.1.11`
   - Description: Generates random decoy IP addresses to obscure the real source.

9. **MAC Address Spoofing**:
   - Command: `nmap -sT -Pn --spoof-mac 0 10.10.1.11`
   - Description: Randomizes the MAC address to appear as a legitimate user.