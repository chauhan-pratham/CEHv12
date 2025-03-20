### Task 3: Enumerate Information from Windows and Samba Hosts using Enum4linux

1. **Open Terminal in Parrot Security**:
   - Switch to the Parrot Security machine and open the terminal.

2. **Gain Root Access**:
   - Type `sudo su` and enter the password (toor).

3. **Run Enum4linux Commands**:
   - **NetBIOS Info**: `enum4linux -u martin -p apple -n 10.10.1.22`
   - **User List**: `enum4linux -u martin -p apple -U 10.10.1.22`
   - **OS Info**: `enum4linux -u martin -p apple -o 10.10.1.22`
   - **Password Policy**: `enum4linux -u martin -p apple -P 10.10.1.22`
   - **Group Policy**: `enum4linux -u martin -p apple -G 10.10.1.22`
   - **Share List**: `enum4linux -u martin -p apple -S 10.10.1.22`

4. **Analyze Output**:
   - Review the output for user accounts, group memberships, OS details, and shared folders.

---

### Conclusion
Document all acquired information from each tool to assess potential vulnerabilities in the target network.