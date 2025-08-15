 
# Amazon Web Scraper

This is a simple Python web scraper designed to extract key product information from an Amazon product page. It uses BeautifulSoup and Requests libraries to fetch and parse the product title, price, rating, number of reviews, and availability status.

## Features

- Extract product title
- Extract product price
- Extract product rating
- Extract the number of user reviews
- Extract product availability status

## How It Works

The scraper sends an HTTP request to the specified Amazon product URL, mimicking a browser with custom headers. It then parses the HTML content with BeautifulSoup to locate and extract specific pieces of product information based on element IDs and class names.

## Requirements

- Python 3.x
- `requests` library
- `beautifulsoup4` library
- `lxml` parser (optional but recommended for faster HTML parsing)

Install the requirements using pip:

pip install requests beautifulsoup4 lxml

 

## Usage

1. Update the `URL` variable in the script with the Amazon product page URL you wish to scrape.
2. Run the script.
3. The script will print extracted product details in the console, such as:

Product Title = Sony PlayStation 4 Pro 1TB Console - Black (PS4 Pro)
Product Price = $XXX.XX
Product Rating = 4.5 out of 5 stars
Number of Product Reviews = 4,190 ratings
Availability = Only 1 left in stock - order soon.

 

## Code Overview

- Modular functions handle extraction of each product attribute.
- Each extraction function uses try-except blocks to manage elements that may be missing on some pages.
- Custom headers prevent request blocking by Amazon servers.
- Uses `lxml` parser with BeautifulSoup for efficient parsing.

## Limitations

- Amazon page structures may change, causing the scraper to fail.
- Price information may sometimes be unavailable or displayed differently.
- Frequent scraping may lead to IP blocking; use responsibly.
- Designed for scraping one product page at a time; bulk scraping requires modification.

## License

This project is licensed under the MIT License.

## Disclaimer

This scraper is intended for educational purposes only. Always ensure scraping aligns with website terms of service.

---

Feel free to extend this scraper by adding support for multiple product scraping, exporting data to files, or integrating with other workflows.
