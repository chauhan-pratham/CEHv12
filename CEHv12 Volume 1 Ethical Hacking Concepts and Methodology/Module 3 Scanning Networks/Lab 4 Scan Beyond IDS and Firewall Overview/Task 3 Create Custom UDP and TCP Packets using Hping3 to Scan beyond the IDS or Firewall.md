1. **Prepare Environment:**
   - Ensure Windows Defender Firewall is enabled on the Windows 11 machine.

2. **Start Packet Capture:**
   - Open Wireshark on Windows 11 and start capturing packets on the Ethernet interface.

3. **Access Parrot Security:**
   - Open a terminal and switch to root user with `sudo su` (password: toor).

4. **Send Random UDP Packets:**
   - Execute the command: 
     ```
     hping3 10.10.1.11 --udp --rand-source --data 500
     ```
   - Observe captured UDP packets in Wireshark on Windows 11.

5. **Send TCP SYN Packets:**
   - Stop the previous command with `Ctrl+C` and run:
     ```
     hping3 -S 10.10.1.11 -p 80 -c 5
     ```
   - Check Wireshark for TCP packets sent to port 80.

6. **Flood Target with TCP Packets:**
   - Run the command:
     ```
     hping3 10.10.1.11 --flood
     ```
   - Monitor the response in the terminal and observe the flooding in Wireshark.

7. **Stop Packet Capture:**
   - Stop capturing packets in Wireshark on Windows 11 and analyze the TCP packet stream.

8. **Disable Windows Firewall:**
   - Turn off Windows Defender Firewall via Control Panel.

9. **Conclusion:**
   - Document findings and consider using other packet crafting tools for similar tasks.

This summary captures the essential steps and commands for using Hping3 to create custom packets while monitoring the results with Wireshark.