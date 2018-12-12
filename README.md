LCNAF-Named-Entity-Reconciliation
=================================

Using OpenRefine and stable, publicly available APIs, the process automatically searches the Virtual International Authority File (VIAF) for matches to personal and corporate names, looks for a Library of Congress source authority record in the matching VIAF cluster, and extracts the authorized heading.  The end result is a dataset, exportable from OpenRefine, with the corresponding authorized LCNAF heading paired with the original name heading, along with a link to the authority record on id.loc.gov

Instructions:
To use this process, please have OpenRefine 2.8 or earlier installed.  This can be downloaded here: http://openrefine.org/download.html

1. Prepare a spreadsheet with the list of names you wish to reconcile in a single column.  The header for this column should be called "Name".  This should be the only column in the spreadsheet.
2. Launch Google Refine.
3. Click "Create Project" and upload the spreadsheet with the names to reconcile.
4. Review the preview screen to make sure the spreadsheet is importing correctly, and click "Create Project".
5. Select the "Apply..." button in top left corner under the "Undo/Redo" tab.
6. Copy the JSON -- that's the entire contents of the text file (PersonalNamesReconcile.txt for personal names only; CorporateNamesReconcile.txt for corporate names only; GenericNamesReconcile.txt for a mix of both personal and corporate names**) -- in its entirety and paste into the pop-up window.  Click "Perform Operations".
7. This will take some time, depending on the time of day and how busy the VIAF servers are. Other tasks can be performed while the process runs in the background. Do not close Google Refine, however.  You can track the progress in the yellow pop-up box at the top of the Google Refine window.  The process will find and remove any duplicate headings in the spreadsheet, so there may be fewer rows in the final results than in the initial spreadsheet.
8. The newly created "LCNAF Heading" column contains the LC authority that matches your original name.  The "LC Record Link" column contains a link to the corresponding LC Authority record.  Any cells without a value have no corresponding LCNAF authority.  You can now export the spreadsheet in any format you choose by using the "Export" function in the upper-right corner of Google Refine.
9. Be sure to double check the accuracy of the matches provided, as VIAF's search algorithm will occasionally provide false matches.

**It is recommended that you separate personal names and corporate names into different spreadsheets and use the corresponding text file (PersonalNamesReconcile.txt or CorporateNamesReconcile.txt) for best results.  You can use GenericNamesReconcile.txt for a spreadsheet consisting of both personal and corporate names if they are too difficult to separate, but the accuracy of the results may be slightly lower.
