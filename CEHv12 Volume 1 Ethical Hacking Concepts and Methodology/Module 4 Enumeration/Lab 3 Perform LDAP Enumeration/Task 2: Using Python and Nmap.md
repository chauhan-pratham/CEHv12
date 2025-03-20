#### Task 2: Using Python and Nmap

1. **Open Terminal:** Switch to Parrot Security and open a terminal.
2. **Gain Root Access:** Type `sudo su` and enter the password (toor).
3. **Nmap Scan:** Run `nmap -sU -p 389 10.10.1.22` to check if port 389 (LDAP) is open.
4. **Brute Force with Nmap:** Execute `nmap -p 389 --script ldap-brute --script-args ldap.base='"cn=users,dc=CEH,dc=com"' 10.10.1.22` to enumerate usernames.
5. **Manual Enumeration with Python:**
   - Start Python shell: `python3`.
   - Import LDAP: `import ldap3`.
   - Connect to LDAP: `server=ldap3.Server('10.10.1.22', port=389)`.
   - Bind connection: `connection=ldap3.Connection(server)` and `connection.bind()`.
   - Retrieve info: `server.info` and perform searches using `connection.search()`.