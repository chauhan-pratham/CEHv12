#### Task 3: Perform DNS Enumeration using Nmap

1. **Nmap DNS Enumeration:**
   - Open a terminal and gain root access: `sudo su` (Password: toor).
   - Discover DNS services: `nmap --script=broadcast-dns-service-discovery www.certifiedhacker.com`.
   - List subdomains: `nmap -T4 -p 53 --script dns-brute www.certifiedhacker.com`.
   - Enumerate service records: `nmap --script dns-srv-enum --script-args "dns-srv-enum.domain='www.certifiedhacker.com'"`.

---

This summary captures the key steps and commands for performing DNS enumeration effectively. Let me know if you need any further modifications or additional information!