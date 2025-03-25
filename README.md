# PDF Metadata Scraper

## Overview

This Python script is designed to automate the process of downloading PDF files from a specified URL and extracting their metadata.  It's particularly useful for gathering information from collections of PDF documents, such as those found in online archives or repositories.

### Key Features
* **PDF Downloading:** Downloads PDF files from a given URL.
* **Metadata Extraction:** Extracts metadata from downloaded PDFs using the `PyPDF2` library.
* **Error Handling:** Robust error handling to manage network issues, PDF reading errors, and other potential problems.
* **Daily Download Organization:** Organizes downloaded PDFs into directories named by date (e.g., `papers/2024-07-24`).
* **Clear Output:** Provides informative output, including the names of downloaded files and their extracted metadata.
* **Robust Link Extraction:** Uses `urljoin` to handle relative and absolute URLs, and verifies that links end with ".pdf".
* **Timeout:** Sets a timeout when downloading PDFs to prevent the script from hanging.
* **Filename Handling:** Extracts filenames from URLs and generates unique names for PDFs without clear filenames.

## Requirements

Before running the script, ensure you have the following installed:

* **Python:** Python 3.6 or later is required.
* **pip:** The Python package installer (usually included with Python).
* **Required Python Libraries:**
    * `requests`: For making HTTP requests to download files.
    * `beautifulsoup4`: For parsing HTML content to find PDF links.
    * `PyPDF2`: For reading PDF files and extracting metadata.

    Install these libraries using pip:

    ```bash
    pip install requests beautifulsoup4 PyPDF2
    ```

## Installation and Setup

1.  **Download the script:** Download the `pdf_metadata_scraper.py` file and save it to your desired location.
2.  **Install dependencies:** Open a terminal or command prompt, navigate to the directory where you saved the script, and run the command:
    ```bash
    pip install requests beautifulsoup4 PyPDF2
    ```

## Usage

1.  **Run the script:** Open a terminal or command prompt, navigate to the directory where you saved the script, and execute it using:
    ```bash
    python pdf_metadata_scraper.py
    ```
2.  **Output:**
    * The script will create a directory named `papers` (or a subdirectory with the current date) in the same directory as the script.
    * Downloaded PDF files will be saved in this directory.
    * The script will print the name of each downloaded file and its extracted metadata to the console.  If a PDF has no metadata, or if there is an error reading the file, this will also be indicated.
