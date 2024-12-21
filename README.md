# WebScraping
On this project, we will extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup.

You will submit the following deliverables:

Deliverable 1: Scrape titles and preview text from Mars news articles.

Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

## Part 1: Scrape Titles and Preview Text from Mars News
Scrape the [Mars News website](https://static.bc-edx.com/data/web/mars_news/index.html) based on these instructions:

-Use automated browsing to visit the Mars news siteLinks to an external site.. Inspect the page to identify which elements to scrape.
-Create a Beautiful Soup object and use it to extract text elements from the website.
-Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
    -Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview. 
    -Store all the dictionaries in a Python list.
    -Print the list in your notebook.
-Store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file

## Part 2: Scrape and Analyze Mars Weather Data
Scrape and analyze [Mars weather data](https://static.bc-edx.com/data/web/mars_facts/temperature.html) based on these instructions:
-Use automated browsing to visit the Mars Temperature Data SiteLinks to an external site.. Inspect the page to identify which elements to scrape. 
-Create a Beautiful Soup object and use it to scrape the data in the HTML table.
-Assemble the scraped data into a Pandas DataFrame
-Analyze your dataset by using Pandas functions to answer the following questions:
    -How many months exist on Mars?
    -How many Martian (and not Earth) days worth of data exist in the scraped dataset?
    -What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
        -Find the average minimum daily temperature for all of the months.
        -Plot the results as a bar chart.
    -Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
        -Find the average daily atmospheric pressure of all the months.
        -Plot the results as a bar chart.
    -About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
        -Consider how many days elapse on Earth in the time that Mars circles the Sun once. Visually estimate the result by plotting the daily minimum temperature of each observation.

#References:
chatgpt to create a scatter plot with hovering data
chart = px.scatter(weather_df,
                x='sol', 
                y='min_temp', 
                title='Min Temperature by Number of Sols',
                hover_data={'sol': True, 'terrestrial_date': True, 'min_temp': True}
                )