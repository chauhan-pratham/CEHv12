### Task 2: Footprinting a Target using Maltego

**1. Launch Maltego:**
   - Open a terminal in Parrot Security and type:
     ```bash
     sudo maltego
     ```
   - Enter the password (`toor`) when prompted.

**2. Set Up Maltego:**
   - A welcome wizard will appear. Select **MALTEGO ID** and click **Next**.
   - If prompted with **Memory Settings Optimized**, click **Restart Now**.
   - Ensure **Online Activation (Default)** is selected and click **Next**.
   - Accept the license agreement and click **Next**.
   - Copy the link provided to log in to Maltego and open it in Firefox.
   - Click **CREATE ID** to create a new Maltego ID, fill in the required details, and verify your email.
   - Return to Maltego and click **Next** after successful login.

**3. Configure Maltego:**
   - Wait for the activation process to complete and click **Next**.
   - Select data sources and click **Next**.
   - Wait for data sources to download and click **Next**.
   - Accept the terms and conditions and click **Next**.
   - Leave the default settings for data source installation and click **Next**.
   - Leave the default options for improving Maltego and click **Next**.
   - Finish the setup.

**4. Create a New Graph:**
   - The Maltego Community Edition GUI will appear. Click on **New Graph (1)**.
   - In the left pane, find the **Entity Palette**. Under **Infrastructure**, drag the **Website** entity onto the graph.
   - Double-click the entity and change the URL to `www.certifiedhacker.com`, then press **Enter**.

**5. Run Transforms:**
   - **To Domains [DNS]**: Right-click the entity and select **All Transforms** > **To Domains [DNS]** to find associated domains.
   - **To DNS Name [Using Name Schema]**: Right-click and select **All Transforms** > **To DNS Name [Using Name Schema]** to identify name schemas.
   - **To DNS Name - SOA**: Right-click and select **All Transforms** > **To DNS Name - SOA** to get the primary name server and admin email.
   - **To DNS Name - MX**: Right-click and select **All Transforms** > **To DNS Name - MX** to identify mail servers.
   - **To DNS Name - NS**: Right-click and select **All Transforms** > **To DNS Name - NS** to find name servers.
   - **To IP Address [DNS]**: Right-click and select **All Transforms** > **To IP Address [DNS]** to get the website's IP address.
   - **To location [city, country]**: Right-click the IP address entity and select **All Transforms** > **To location [city, country]** to determine geographical location.
   - **To Entities from WHOIS**: Right-click the domain entity and select **All Transforms** > **To Entities from WHOIS [IBM Watson]** to gather ownership information.

**6. Personal Information Gathering:**
   - In the left pane, click the **Personal** node under Entity Palette to extract information about employees, such as email addresses and phone numbers.

**7. Document Findings:**
   - Close all open windows and document the information gathered for future reference.

---

