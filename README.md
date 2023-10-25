# web scraping and data analysis project

I used the knowledge I've learned to identify HTML elements on a page, identify their id and class attributes, scrape various types of information, including HTML tables and recurring elements, like multiple news articles on a webpage. I extracted information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. 

* This analysis consists of two technical products, the deliverables includes:
  * Deliverable 1: Scrape titles and preview text from Mars news articles.
  * Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

# Part 1: Scrape Titles and Preview Text from Mars News
* In this part, I used automated browsing to visit https://static.bc-edx.com/data/web/mars_news/index.html 
* Inspected the page to identify which elements to scrape.
* I created a Beautiful Soup object and use it to extract text elements from the website.
* I extracted the titles and preview text of the news articles that I scraped. 
* Stored the scraping results, each title-and-preview pair in a Python dictionary and, gave each dictionary two keys: title and preview. 
* Stored all the dictionaries in a Python list.

![Alt text](<Screenshot 2023-10-25 032833-1.png>)

* Printed the list in my Jupyter Notebook.

# Part 2: Scrape and Analyze Mars Weather Data
I used automated browsing to visit https://static.bc-edx.com/data/web/mars_facts/temperature.html
* Inspected the page to identify which elements to scrape.
* I created a Beautiful Soup object and use it to scrape the data in the HTML table.
* I assembled the scraped data into a Pandas DataFrame. The columns had the same headings as the table on the website. Here’s an explanation of the column headings:
  * id: the identification number of a single transmission from the Curiosity rover
      terrestrial_date: the date on Earth
  * sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
  * ls: the solar longitude
  * month: the Martian month
  * min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
  * pressure: The atmospheric pressure at Curiosity's location

* I examined the data types that are currently associated with each column. I converted the data to the appropriate datetime, int, or float data types.
* I analyzed the dataset by using Pandas functions to answer the following questions:
  * How many months exist on Mars?
  * How many Martian (and not Earth) days worth of data exist in the scraped dataset?
  * What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
      * Find the average minimum daily temperature for all of the months.
      * Plot the results as a bar chart.
  * Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
     * Find the average daily atmospheric pressure of all the months.
    * Plot the results as a bar chart.
* About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
     * Consider how many days elapse on Earth in the time that Mars circles the Sun once.
     * Visually estimate the result by plotting the daily minimum temperature.

* I exported the DataFrame to a CSV file.
