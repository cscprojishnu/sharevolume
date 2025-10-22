# Company Shares Data Dashboard

This is a single-file, responsive HTML application designed to display the maximum and minimum shares outstanding for a given company, fetched directly from the SEC's XBRL API.

## Features

- **Dynamic Data Fetching**: Retrieves company shares outstanding data based on CIK (Central Index Key).
- **Responsive Design**: Built with Tailwind CSS for a seamless experience across various devices.
- **Max/Min Shares Display**: Clearly highlights the highest and lowest shares outstanding for fiscal years after 2020.
- **CIK Parameter Support**: Load data for any company by appending a `CIK` query parameter to the URL.

## Setup and Usage

1.  **Save the file**: Save the `index.html` content as `index.html` in your local directory.
2.  **Open in Browser**: Open `index.html` in any modern web browser.

    By default, it will display data for **Broadcom Inc. (CIK: 0001730168)**.

3.  **Load Data for a Different Company**: To view data for another company, append a `?CIK=<your_cik_number>` query parameter to the URL. For example:

    `index.html?CIK=0001018724` (for Apple Inc.)

    The application will then fetch and display the relevant data without requiring a page reload.

## Data Source

Data is fetched from the SEC's XBRL API endpoint for `EntityCommonStockSharesOutstanding`.

- `https://data.sec.gov/api/xbrl/companyconcept/CIK<CIK_NUMBER>/dei/EntityCommonStockSharesOutstanding.json`

Note: A public CORS proxy (`https://api.allorigins.win/raw?url=`) is used for client-side fetches to bypass CORS restrictions when accessing the SEC API directly from the browser. For server-side applications, ensure a descriptive `User-Agent` is set as per SEC guidance.

## Included Attachment

The content of `uid.txt` is embedded directly into the HTML page for demonstration purposes, as requested.

## Technologies Used

- HTML5
- Tailwind CSS (CDN)
- JavaScript (ES6+)

## License

This project is open-sourced under the MIT License. See the `LICENSE` file for details.
