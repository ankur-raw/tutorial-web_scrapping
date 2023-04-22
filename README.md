# tutorial-web_scrapping
This project is used to scrap data from desired website
This is a Python project that is used to scrape data from a website. The function is designed to extract the name of the author, quotes, and tags from a website called "http://quotes.toscrape.com/".

The function scrap_data() begins by creating an empty list called "Content" to store the scraped data. It then sets a variable called "i" to 1, indicating that it will begin scraping data from page 1 of the website.

The function uses a while loop to iterate through all the available pages of the website. It does this by dynamically creating a URL for each page using string interpolation and requests the HTML content of the page using the requests library. The HTML content is then parsed using the BeautifulSoup library.Also, using while loop here to check all the available pages which has information which we require i.e name, quotes and tags.Using this here because we don't know the number of pages available, to get rid of manually checking all the pages we are using while loop here which will do all the work for us automatically. If no required data is found the while loop will break.

The function then uses a for loop to iterate through all the quote elements on the page and extracts the name of the author, the quote text, and the tags associated with the quote. This data is then appended to the "Content" list.

Once all the pages have been scraped, the function calls another function called "save_as_csv" to save the scraped data to a CSV file.

The "save_as_csv" function takes the "Content" list as an input parameter and converts it into a Pandas DataFrame. The DataFrame is then saved as a CSV file called "quote_Scrap.csv".

Overall, this function is a useful tool for anyone who needs to scrape data from websites, especially for those who need to extract information from multiple pages of a website.
