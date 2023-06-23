# Downloading_tool
The APP has GUI and downloading pdfs from text file to given folder 

Final version - 2 files:

* file_bulk_downloader.py - downloads files from links and get links from web-page, saves log into download_details.csv

* web_bulk_downloader.py - downloads web-pages from links to pdf file.

## Dependancies

[https://wkhtmltopdf.org/downloads.html](https://wkhtmltopdf.org/downloads.html)



## Instructions for testing

### Test 1: Downloading PDF files from a URL file
1. Prepare a text file (`urls.txt`) containing a list of URLs, each URL on a separate line.
2. Run the script.
3. Click the "Browse" button next to the "Select the file with the list of URLs" label and select the `urls.txt` file.
4. Click the "Browse" button next to the "Select the folder to save the files" label and choose a directory to save the downloaded files.
5. Click the "Start Download" button.
6. Observe the progress in the text window and check if the PDF files are downloaded successfully.

### Test 2: Canceling the download
1. Repeat steps 1-5 from Test 1.
2. After clicking the "Start Download" button, click the "Cancel" button.
3. Observe if the script stops downloading and the progress stops updating.

### Test 3: Handling errors
1. Modify the `urls.txt` file to include a URL that does not exist or returns an error status code.
2. Repeat steps 2-5 from Test 1.
3. Observe if the script correctly handles the error and logs the error message in the CSV file and progress text.

### Test 4: Resuming from a previous session
1. Perform Test 1 to download some files and log the progress.
2. Repeat steps 1-5 from Test 1, using the same `urls.txt` file.
3. Observe if the script skips the URLs that were already processed in the previous session and logs them as "Already downloaded" in the progress text.

### Test 5: Checking the CSV log
1. Perform Test 1 to download some files.
2. Open the `download_details.csv` file to inspect the logged information.
3. Check if the CSV file contains the expected columns (Original Link, Final Response Link, Filename, Status) and if the information is correctly logged for each download.
