#### Task 1: Perform DNS Enumeration using Zone Transfer

1. **DNS Enumeration on Linux:**
   - Open a terminal in Parrot Security and gain root access: `sudo su` (Password: toor).
   - Retrieve name servers: `dig ns www.certifiedhacker.com`.
   - Attempt zone transfer: `dig @ns1.bluehost.com www.certifiedhacker.com axfr`. (Expect "Transfer failed" if not allowed.)

2. **DNS Enumeration on Windows:**
   - Open Command Prompt and enter `nslookup`.
   - Set query type: `set querytype=soa`.
   - Query target domain: `certifiedhacker.com`.
   - Attempt zone transfer: `ls -d ns1.bluehost.com`. (Expect "refused" if not allowed.)