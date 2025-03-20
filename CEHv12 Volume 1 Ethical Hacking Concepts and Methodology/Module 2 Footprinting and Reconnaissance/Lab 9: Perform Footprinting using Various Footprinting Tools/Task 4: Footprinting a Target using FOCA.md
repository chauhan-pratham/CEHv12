### Task 4: Footprinting a Target using FOCA

**1. Switch to Windows Server 2019:**
   - Click on the Windows Server 2019 machine.
   - Press `Ctrl + Alt + Delete` to activate the machine.
   - Log in using the password `Pa$$w0rd`.

**2. Launch FOCA:**
   - Navigate to the directory: `Z:\CEHv12 Module 02 Footprinting and Reconnaissance\Footprinting Tools\FOCA`.
   - Double-click `FOCA.exe` to launch the application.

**3. Create a New Project:**
   - In the FOCA main window, go to **Project** and click **New Project**.
   - Fill in the project details:
     - **Project name**: `Project of www.eccouncil.org`
     - **Domain website**: `www.eccouncil.org`
     - Leave **Alternative domains** empty.
     - Click the folder icon to choose a save location (e.g., Desktop).
   - Click **Create** to save the project.

**4. Gather Information:**
   - Select all three search engines: Google, Bing, and DuckDuckGo.
   - Under **Extensions**, select **All** to include all file types.
   - Click the **Search All** button to start gathering information.

**5. View Results:**
   - Once the search is complete, the results will display metadata associated with the target domain.
   - Right-click on any URL to open it in a web browser to view the extracted files.

**6. Analyze Network Structure:**
   - In the left pane, click on the **Network** node to expand it and view the network structure.
   - If there are associated clients or servers, they will be displayed here.

**7. Perform Google Crawling:**
   - Expand the **Domains** node and click on the target domain (e.g., `eccouncil.org`).
   - Click the **Crawling** tab and then click the **Google crawling** button to start crawling the website.
   - Review the results, which will include domains obtained through scanning and their severity levels.

**8. Document Metadata Summary:**
   - Expand the **Document Analysis** node and then the **Metadata Summary** node to view information regarding users, folders, and software.
   - Document all relevant findings.

**9. Close and Document:**
   - Close all open windows and document all acquired information.
