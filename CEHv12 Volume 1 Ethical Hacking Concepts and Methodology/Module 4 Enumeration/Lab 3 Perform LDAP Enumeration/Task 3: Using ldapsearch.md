#### Task 3: Using ldapsearch

1. **Open Terminal:** In Parrot Security, open a terminal.
2. **Gain Root Access:** Type `sudo su` and enter the password (toor).
3. **Query Naming Contexts:** Run `ldapsearch -h 10.10.1.22 -x -s base namingcontexts`.
4. **Retrieve Domain Info:** Execute `ldapsearch -h 10.10.1.22 -x -b "DC=CEH,DC=com"`.
5. **Enumerate All Objects:** Use `ldapsearch -x -h 10.10.1.22 -b "DC=CEH,DC=com" "objectclass=*"`.

---

This summary captures the key steps and commands for performing LDAP enumeration effectively. Let me know if you need any further modifications!