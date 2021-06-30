# Data scraping from e-commerce website

This is my weekly project in CoderSchool with Ha.

## Goal
The goal of this weekly project is to crawl products from all categories of an e-commerce website, in this case is Tiki.vn.

For each main categories, the notebook will start to crawl links for sub categories, and then recursively looking into deeper level of sub categories( Main -> level 2 -> level 3 -> level 4 -> ... ). 
When it reachs the deepest level (no sub categories), then will crawl information of all the products in that categories.

Information of crawled items and category links will be saved in a SQLite database.

As the number of products is quite large, we just managed to scrape as many products as we could during the weekend. We didn't have time to analyze them.

## Libraries used:

To complete this project, we need
- `Selenium`: to retrieve the HTML code in our website
- `BeatifulSoup`: to parse the HTML code and get relavant information through HTML tags
- `SQLite`: to manage our database

## Files:
- `cs_tiki_scraping.ipynb`: Jupyter notebook we made to scrape the data
- `tiki.db`: the database containing scraped data
    
    - Table `categories`: contains information about main and sub categories scraped
    - Table `products`: contains data about products scraped