### Lab 9: Perform Footprinting using Various Footprinting Tools

#### Lab Scenario
As an ethical hacker, you need to gather comprehensive information about a target to identify potential vulnerabilities. This lab demonstrates how to extract additional information using various footprinting tools.

#### Objectives
- Footprinting a target using:
  - Recon-ng
  - Maltego
  - OSRFramework
  - FOCA
  - BillCipher
  - OSINT Framework

### Overview of Footprinting Tools
Footprinting tools collect essential information about target systems, including:
- IP location
- Routing information
- Business details (address, phone number)
- Email source and file details
- DNS and domain information

### Task 1: Footprinting a Target using Recon-ng

1. **Switch to Parrot Security Machine**:
   - Click on Parrot Security-M2 to access the machine.

2. **Open Terminal**:
   - Click the MATE Terminal icon to open a terminal window.

3. **Gain Root Access**:
   - Type `sudo su` and press Enter.
   - Enter the password `toor` (it will not be visible).

4. **Launch Recon-ng**:
   - Type `cd` to go to the root directory.
   - Type `recon-ng` and press Enter to start the application.

5. **Install Modules**:
   - Type `help` to view available commands.
   - Type `marketplace install all` to install all modules (ignore any errors).
   - Type `modules search` to view all available modules.

6. **Create a Workspace**:
   - Type `workspaces create CEH` to create a new workspace named CEH.
   - Type `workspaces list` to view existing workspaces.

7. **Add Target Domain**:
   - Type `db insert domains` and press Enter.
   - Enter `certifiedhacker.com` as the domain and press Enter.
   - Type `show domains` to confirm the addition.

8. **Harvest Hosts Information**:
   - Load the brute_hosts module:
     - Type `modules load recon/domains-hosts/brute_hosts` and press Enter.
   - Type `run` to start harvesting hosts.

9. **Use Additional Modules**:
   - To use the Bing module for host harvesting:
     - Type `back` to return to the CEH terminal.
     - Type `modules load recon/domains-hosts/bing_domain_web` and press Enter.
     - Type `run` to execute.

10. **Perform Reverse Lookup**:
    - Load the reverse_resolve module:
      - Type `modules load recon/hosts-hosts/reverse_resolve` and press Enter.
    - Type `run` to perform the reverse lookup.
    - Type `show hosts` to display all harvested hosts.

11. **Generate a Report**:
    - Load the reporting module:
      - Type `modules load reporting/html` and press Enter.
    - Set report options:
      - Type `options set FILENAME /home/attacker/Desktop/results.html` and press Enter.
      - Type `options set CREATOR Jason` and press Enter.
      - Type `options set CUSTOMER Certifiedhacker Networks` and press Enter.
    - Type `run` to generate the report.

12. **View the Report**:
    - Navigate to the Desktop and open `results.html` in Firefox to view the report.

### Gathering Personnel Information
1. **Open a New Terminal**:
   - Type `sudo su` and enter the password `toor`.

2. **Launch Recon-ng Again**:
   - Type `recon-ng` and press Enter.

3. **Create a New Workspace**:
   - Type `workspaces create reconnaissance` and press Enter.

4. **Extract Contacts**:
   - Load the whois_pocs module:
     - Type `modules load recon/domains-contacts/whois_pocs` and press Enter.
   - Set the target domain:
     - Type `options set SOURCE facebook.com` and press Enter.
   - Type `run` to extract contacts.

5. **Document Contacts**:
   - Note down the contacts obtained from the results.

### Extract Subdomains and IP Addresses
1. **Open a New Terminal**:
   - Type `sudo su` and enter the password `toor`.

2. **Launch Recon-ng**:
   - Type `recon-ng` and press Enter.

3. **Load Hackertarget Module**:
   - Type `modules load recon/domains-hosts/hackertarget` and press Enter.
   - Set the target domain:
     - Type `options set SOURCE certifiedhacker.com` and press Enter.
   - Type `run` to extract subdomains and IP addresses.

### Conclusion
- Close all open windows and document all acquired information, including screenshots and notes on harvested hosts, personnel information, and subdomains. This comprehensive data will assist in identifying potential vulnerabilities in the