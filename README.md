LCNAF-Named-Entity-Reconciliation
=================================

Using OpenRefine and stable, publicly available APIs, the process automatically searches the Virtual International Authority File (VIAF) for matches to personal and corporate names, looks for a Library of Congress source authority record in the matching VIAF cluster, and extracts the authorized heading.  The end result is a dataset, exportable from OpenRefine, with the corresponding authorized LCNAF heading paired with the original name heading, along with a link to the authority record on id.loc.gov

Instructions:
To use this process, please have Google Refine v.2.5-r2407 installed.  This can be downloaded here: http://openrefine.org/download.html

1. Prepare a spreadsheet with the list of names you wish to reconcile in a single column.  The header for this column should be called "Name".  Separate personal names and corporate names into different spreadsheets.
2. Launch Google Refine.
3. Click "Create Project" and upload the spreadsheet with the names to reconcile.
4. Review the preview screen to make sure the spreadsheet is importing correctly, and click "Create Project".
5. Select the "Apply..." button in top left corner under the "Undo/Redo" tab.
6. Copy the JSON—that's all the text in the text file (PersonalNamesReconcile.txt for personal names; CorporateNamesReconcile.txt for corporate names)-- in its entirety and paste into the pop-up window.  Click "Perform Operations".
7. This will take some time, depending on the time of day and how busy the VIAF servers are. Other tasks can be performed while the process runs in the background. Do not close Google Refine, however.  You can track the progress in the yellow pop-up box at the top of the Google Refine window.
8. The newly created "LCNAF Heading" column contains the LC authority that matches your original name.  The "LC Record Link" column contains a link to the corresponding LC Authority record.  Any cells without a value have no corresponding LCNAF authority.  You can now export the spreadsheet in any format you choose by using the "Export" function in the upper-right corner of Google Refine.
