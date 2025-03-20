### Task 5: Footprinting a Target using BillCipher

**1. Switch to Parrot Security:**
   - Click on the Parrot Security-M2 machine.
   - Open the MATE Terminal.

**2. Run as Root:**
   - Type the following command to switch to the root user:
     ```bash
     sudo su
     ```
   - Enter the password (`toor`).

**3. Navigate to BillCipher Directory:**
   - Change to the BillCipher directory:
     ```bash
     cd BillCipher
     ```

**4. Launch BillCipher:**
   - Start the application by typing:
     ```bash
     python3 billcipher.py
     ```

**5. Collect Information:**
   - When prompted, type `website` to collect information about a website.
   - Enter the target website URL (e.g., `www.certifiedhacker.com`).

**6. Perform Various Lookups:**
   - Choose the following options to gather information:
     - **DNS Lookup**: Type `1` and press Enter.
     - **GeoIP Lookup**: Type `3` and press Enter.
     - **Subnet Lookup**: Type `4` and press Enter.
     - **Page Links**: Type `6` and press Enter.
     - **HTTP Header**: Type `8` and press Enter.
     - **Host Finder**: Type `9` and press Enter.

**7. Continue Gathering Information:**
   - After each lookup, type `Yes` to continue collecting more information.

**8. Document Findings:**
   - Close all open windows and document all the acquired information.