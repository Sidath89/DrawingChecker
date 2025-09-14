# Drawing Checker

A Windows utility for architects, engineers, and construction professionals to automatically verify drawing registers against project folders. Quickly identifies missing drawings, additional files, and checks for document compliance.

## The Problem

In any large-scale construction or engineering project, managing hundreds or thousands of drawings is a critical task. A drawing register (usually an Excel sheet) serves as the master list, but ensuring that every file listed in the register exists in the project folder and that no extra, unlisted files are present is a tedious and error-prone manual process. A single mistake can lead to outdated plans being used on-site, causing significant delays and costs.

This tool automates that entire verification process in seconds.

## Key Features

* **Automated Verification:** Directly compares a drawing list from an Excel file against the contents of a specified folder.
* **Identify Missing Drawings:** Instantly generates a list of all drawings that are in the register but are not found in the folder.
* **Find Additional Drawings:** Creates a list of all files that exist in the folder but are not listed in the register, helping to identify unofficial or outdated revisions.
* **Detailed Compliance View:** For drawings that are found, the tool checks for the presence of required file formats (e.g., PDF, DWG) and displays a clear compliance status.
* **Export Results:** All findings can be exported to a clean Excel or CSV report for easy sharing and record-keeping.

## How to Use the Drawing Checker

Here is a step-by-step guide to operating the software.

#### Step 1: Select Your Inputs

1.  **Excel File:** Click the `Browse...` button to select the Excel drawing register you want to check.
2.  **Drawings Folder:** Click the second `Browse...` button to select the main folder where all your project drawings are stored.

#### Step 2: Configure the Data Source

3.  **Sheet:** Once you select an Excel file, this dropdown will populate with all the sheet names from that workbook. Choose the sheet that contains your drawing list.
4.  **Column:** This dropdown will show all the columns from the selected sheet. Choose the column that contains the drawing numbers (e.g., "A", "B", "C").
5.  **Data Starting Row:** Enter the row number where your list of drawing numbers begins (e.g., if there are headers, your list might start on row `17`).

#### Step 3: Run the Analysis

6.  Click the **`Find Missing Drawings`** button. The application will read the Excel file, scan the folder, and perform the comparison.

#### Step 4: Review the Results

The results are displayed across three tabs:

* **`Summary / Action Items` Tab:**
    * **Missing Drawings:** This list shows all drawings from the register that were ***not*** found in the folder.
    * **Additional Drawings:** This list shows all files found in the folder that were ***not*** in the register.
    * `Move Selected to Additional Drawings`: Select one or more files from the **Additional Drawings** list and click this button to move them into a dedicated subfolder for review.
    * `Delete Selected`: Permanently deletes selected files from the **Additional Drawings** list.

* **`Detailed Matched View` Tab:**
    * This grid shows all the drawings from the register that were **successfully found** in the folder.
    * It includes columns indicating whether a `PDF`, `DWG`, or other file type exists for that drawing number.
    * The **Compliance** column tells you if the drawing meets the required file criteria (e.g., "Must have both PDF and DWG").

* **`Master List` Tab:**
    * This is a simple, complete list of all the drawing numbers that were successfully read from your selected Excel sheet and column.

#### Step 5: Export Your Report

7.  Click the **`Export to Excel`** button. This will allow you to save a comprehensive report of the missing, additional, and matched drawings to an Excel or CSV file.

## Getting Started (Installation)

1.  Go to the [**Releases Page**](https://github.com/Sidath89/DrawingChecker/blob/main/Drawing%20Checker.zip) of this repository.
2.  Download the `.zip` file from the latest release.
3.  Unzip the downloaded file to a folder on your computer.
4.  Run `DrawingChecker.exe`.

> **Note on Windows Security:**
> When you run the `.exe` for the first time, Windows Defender SmartScreen may show a security warning. This is normal for new applications from independent developers. To run the program, click **"More info"** and then **"Run anyway"**.

## Contributing & Future Plans

This is my first piece of software, and while it's designed to be robust, it might not be perfect. I warmly welcome any suggestions, bug reports, and ideas for new features! The best way to contribute is to open a new **"Issue"** on this GitHub repository.

**Next on the roadmap:**

* Implement a feature to read and compare rates/costs from tenderer documents to assist with financial analysis.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.
