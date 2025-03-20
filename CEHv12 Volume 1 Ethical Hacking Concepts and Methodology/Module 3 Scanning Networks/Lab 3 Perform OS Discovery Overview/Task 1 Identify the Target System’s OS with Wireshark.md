### Task 1: Identify the Target System’s OS with Wireshark

1. **Launch Wireshark**:
   - Open Wireshark on the Windows 11 machine.

2. **Start Packet Capture**:
   - Double-click the Ethernet interface to begin capturing packets.

3. **Ping Windows Server**:
   - Open Command Prompt and run: `ping 10.10.1.22`.

4. **Analyze ICMP Reply**:
   - Select an ICMP reply packet from the Windows Server.
   - Expand the Internet Protocol Version 4 node to find the TTL value (e.g., 128 indicates Windows).

5. **Stop Capture**:
   - Click the Stop button in Wireshark.

6. **Ping Ubuntu Machine**:
   - Run: `ping 10.10.1.9` in Command Prompt.

7. **Analyze ICMP Reply**:
   - Select an ICMP reply packet from the Ubuntu machine.
   - TTL value of 64 indicates a Linux-based OS.

8. **Stop Capture**:
   - Click the Stop button in Wireshark.