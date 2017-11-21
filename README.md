# importJSON_to_gsheets
Short instructions

The instructions are from <a href="https://medium.com/@paulgambill/how-to-import-json-data-into-google-spreadsheets-in-less-than-5-minutes-a3fede1a014a" target="_blank">here</a>.

1. From your Google Spreadsheet, click on Tools -> Script Editor.
2. Click Create script for Spreadsheet.
3. Delete the placeholder content and paste the code from this script.
4. Paste the code from the `script.gs` file. 
5. Rename the script to ImportJSON.gs and click the save button.
6. Back in the spreadsheet, use the function by invoking e.g. `=ImportJSON("https://api.openaq.org/v1/measurements?coordinates=51.5291019,-0.1077666", "/meat", "noInherit, noTruncate")`
