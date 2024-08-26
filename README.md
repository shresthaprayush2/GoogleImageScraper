# GoogleImageScraper
A beginner-friendly web scraping project using Python, Selenium, and Pandas to automate the process of fetching and downloading product images from Google based on product names, sizes, and container types. Initially developed to help a client build an online liquor delivery system by quickly gathering product images. 


## Project Background

This project was developed to assist a client who was building an online liquor delivery system. They had manually collected the product names, sizes, and container types but needed a fast and efficient way to gather product images. This scraper is the first iteration to fetch images, regardless of quality, providing a quick solution to get the project rolling.

## Features

- **Automated Image Scraping**: The script automatically searches for and downloads images based on the product details provided in a CSV file.
- **Optimized for Performance**: The Selenium browser is configured with performance tweaks to make the scraping process faster.
- **Beginner-Friendly**: The code is designed to be easy to understand and modify, making it a great learning resource for those new to web scraping.

## How It Works

1. **Setting Up Selenium**: The script optimizes Selenium's performance by disabling unnecessary features like extensions and notifications, and runs in headless mode.
2. **Loading Data**: It reads product data from a CSV file, including the product name, size, and container type.
3. **Generating Search URLs**: The product information is formatted into a search-friendly string, which is then used to query Google Images.
4. **Downloading Images**: The script waits for Google to load the search results, then extracts the image link and downloads it, saving the image with a product-specific filename.

## Prerequisites

- Python 3.x
- Selenium (`pip install selenium`)
- Pandas (`pip install pandas`)
- Chrome WebDriver (Ensure it's compatible with your version of Chrome)

## Installation

1. Clone the repository:
  
2. Install the required Python packages:
   
## Usage

1. Place your product data in a CSV file named `WineData.csv`. The CSV should have columns for `Product Name`, `Size1`, and `container`.
2. Run the scraper:
    
3. The images will be downloaded to the project directory with filenames based on the product names.

## Challenges and Solutions

### The Case of the Disappearing Images
One of the key challenges was Google's dynamic loading of images and tags, which caused the scraper to miss some images. This was resolved by adding a wait condition using Selenium’s `WebDriverWait` and `expected_conditions`.

## Future Improvements

- Enhance the scraper to filter for higher-quality images.
- Integrate with APIs for more precise image results.
- Expand the script to handle more complex search queries and dynamic content.


Contributions are welcome! Please feel free to submit a Pull Request or open an issue for any suggestions or improvements.

---

*Happy Scraping! 🍷*
