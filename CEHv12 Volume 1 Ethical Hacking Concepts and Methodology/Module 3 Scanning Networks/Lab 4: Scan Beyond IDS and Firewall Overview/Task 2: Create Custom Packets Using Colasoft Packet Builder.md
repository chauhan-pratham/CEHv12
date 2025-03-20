### Task 2: Create Custom Packets Using Colasoft Packet Builder

1. **Switch to Windows Server 2019**:
   - Log in with username `Administrator` and password `Pa$$w0rd`.

2. **Launch Wireshark**:
   - Open Wireshark and start capturing packets on the Ethernet interface.

3. **Launch Colasoft Packet Builder**:
   - Open Colasoft Packet Builder.

4. **Select Adapter**:
   - Choose the appropriate network adapter.

5. **Add ARP Packet**:
   - Click the Add icon, select ARP Packet template, and set Delta Time to 0.1 seconds.

6. **Edit Packet Information**:
   - Use the Decode Editor and Hex Editor to modify packet details as needed.

7. **Send Packets**:
   - Click Send, select Burst Mode, and start sending packets.

8. **Capture ARP Responses**:
   - In Wireshark, filter for ARP packets to observe responses from active machines.

9. **Export Packets**:
   - Export the created packets for future reference.

### Conclusion
This lab demonstrated various techniques to scan beyond IDS and firewalls using Nmap and custom packet creation with Colasoft Packet Builder. Document all findings for future analysis and reference.