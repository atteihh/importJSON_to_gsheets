# importJSON_to_gsheets
Short instructions

The instructions are from <a href="https://medium.com/@paulgambill/how-to-import-json-data-into-google-spreadsheets-in-less-than-5-minutes-a3fede1a014a" target="_blank">here</a>.

1. From your Google Spreadsheet, click on Tools -> Script Editor.
2. Click Create script for Spreadsheet.
3. Delete the placeholder content and paste the code from this script.
4. Paste the code from the `script.gs` file. 
5. Rename the script to ImportJSON.gs and click the save button.
6. In Google sheets, the function to use is `=ImportJSON()`.

## Using the API

We will use Breezometer to collect air quality data. The documentation is here:
```
https://breezometer.com/air-quality-api/
```

An example of how to use the API is like this:
```
https://api.breezometer.com/baqi/?lat=51.5286263&lon=-0.1057266&key=2156295a3962496aace88a0a38c25ac3
```

Change the latitude and longitude.

To read the data into the Google Spreadsheet do:
```
=transpose(importJSON("https://api.breezometer.com/baqi/?lat=51.5291019&lon=-0.1077666&key=2156295a3962496aace88a0a38c25ac3","/breezometer_description","noInherit, noTruncate"))
```

And to format it correctly, do:
```
=transpose(importJSON("https://api.breezometer.com/baqi/?lat=51.5291019&lon=-0.1077666&key=2156295a3962496aace88a0a38c25ac3","/breezometer_description","noInherit, noTruncate"))
```

An alternative API keys is: `df38c88a6193447dac1aae3c8bfb0475`.
