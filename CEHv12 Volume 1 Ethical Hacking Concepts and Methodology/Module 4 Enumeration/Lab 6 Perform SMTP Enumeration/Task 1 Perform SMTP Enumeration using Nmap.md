### SMTP Enumeration Lab Overview

**Objective:** Gather information about valid users and delivery addresses on an SMTP server.

#### Task 1: Perform SMTP Enumeration using Nmap

1. **Open Terminal:**
   - Launch the terminal in Parrot Security.
   - Gain root access: `sudo su` (Password: toor).

2. **Enumerate SMTP Users:**
   - Run the command: `nmap -p 25 --script=smtp-enum-users 10.10.1.19`.
     - This command lists all possible mail users on the SMTP server.

3. **Check for Open SMTP Relays:**
   - Execute: `nmap -p 25 --script=smtp-open-relay 10.10.1.19`.
     - This command identifies any open SMTP relays on the server.

4. **List Available SMTP Commands:**
   - Run: `nmap -p 25 --script=smtp-commands 10.10.1.19`.
     - This command displays all SMTP commands available on the target host.

---

This summary captures the key steps and commands for performing SMTP enumeration effectively. Let me know if you need any further modifications or additional information!