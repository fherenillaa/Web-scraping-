# Scraping Sephora's website using html
The code above performs web scraping and crawling to obtain data from the Sephora Indonesia website regarding makeup products. Here’s a breakdown of the steps:

1. Import Libraries:
BeautifulSoup is used for parsing HTML and extracting data from the website.
requests sends HTTP requests to retrieve web pages.
pandas is utilized to store data in a tabular format and export it to a CSV file.

2. Initialize Data:
Several empty lists are defined to store data such as brand, product name, price, number of reviews, variants, and product images.

3. Loop for Crawling:
In the for page in range(1, 36) loop, the crawler accesses pages from 1 to 35. The URL for each page is constructed by appending the page number to the root URL.
For each page, the HTML content is fetched using rs.get(url) and parsed with BeautifulSoup.

4. Scraping Data:
The scraping(soup) function searches for all products on the page using the <div class="product-card"> tag.
For each product, data is extracted, such as the brand, product name, price, number of reviews, variants, and product image links.
This data is stored in their respective lists after stripping to remove excess whitespace.

5. Creating a DataFrame:
After scraping all pages, the data is stored in a pandas DataFrame with appropriate columns.
The DataFrame is then exported to a CSV file named "Produk Make Up Sephora Indonesia.csv"

6. Output:
The results of the scraping are displayed with df.head(), which shows the first 5 rows, and the CSV file is saved to the system.

This technique helps automate the extraction of data from multiple web pages simultaneously using web crawling.
