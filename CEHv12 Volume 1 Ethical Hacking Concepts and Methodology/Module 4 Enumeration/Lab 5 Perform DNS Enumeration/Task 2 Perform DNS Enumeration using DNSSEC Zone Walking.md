#### Task 2: Perform DNS Enumeration using DNSSEC Zone Walking

1. **Use DNSRecon Tool:**
   - Open a terminal and gain root access: `sudo su` (Password: toor).
   - Navigate to the DNSRecon directory: `cd dnsrecon`.
   - Make the script executable: `chmod +x ./dnsrecon.py`.
   - View options: `./dnsrecon.py -h`.
   - Perform DNSSEC zone walking: `./dnsrecon.py -d www.certifiedhacker.com -z`.
   - Review enumerated DNS records.