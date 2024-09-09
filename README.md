# data_scraping

# Credits:
This code was written based off the starter code and completed by Lauren Graves. Trouble shooting assisted through Expert Learning Assistant.
Nasa Science site was referenced during analysis for confirmation of Mars' days (reference link : https://science.nasa.gov/mars/facts/).

# Background
You’re now ready to take on a full web-scraping and data analysis project. You’ve learned to identify HTML elements on a page, identify their id and class attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. You’ve also learned to scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.

As you work on this Challenge, remember that you’re strengthening the same core skills that you’ve been developing until now: collecting data, organizing and storing data, analyzing data, and then visually communicating your insights.

# Part 1: Scrape Titles and Preview Text from Mars News
-Open the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. You will work in this code as you follow the steps below to scrape the Mars News website.
1.Use automated browsing to visit the Mars news siteLinks to an external site.. Inspect the page to identify which elements to scrape.
2.Create a Beautiful Soup object and use it to extract text elements from the website.
3.Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
-Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview
-Store all the dictionaries in a Python list.
-Print the list in your notebook.
4.Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file. (Note: there will be no extra points for completing this.)

# Part 2: Scrape and Analyze Mars Weather Data
Open the Jupyter Notebook in the starter code folder named part_2_mars_weather.ipynb. You will work in this code as you follow the steps below to scrape and analyze Mars weather data.
1.Use automated browsing to visit the Mars Temperature Data SiteLinks to an external site.. Inspect the page to identify which elements to scrape. Note that the URL is https://static.bc-edx.com/data/web/mars_facts/temperature.html.
2.Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.
3.Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
-id: the identification number of a single transmission from the Curiosity rover
-terrestrial_date: the date on Earth
-sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
-ls: the solar longitude
-month: the Martian month
-min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
-pressure: The atmospheric pressure at Curiosity's location
4.Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
5.Analyze your dataset by using Pandas functions to answer the following questions:
-How many months exist on Mars? 12

-How many Martian (and not Earth) days worth of data exist in the scraped dataset? 1867

-What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
    -Find the average minimum daily temperature for all of the months.
    -Plot the results as a bar chart.
    Based on the analysis performed with the data, Mars' third month has the lowest average temperature. The eigth month has the highest average temperture.
    
-Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    -Find the average daily atmospheric pressure of all the months.
    -Plot the results as a bar chart.
    Based on the analysis performed with the data, Mars' sixth month has the lowest atmospheric pressure. The ninth month has the highest atmospheric pressure. 
    
-About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
    -Consider how many days elapse on Earth in the time that Mars circles the Sun once.
    -Visually estimate the result by plotting the daily minimum temperature of each observation.
    Based on the visual created using the data, we can see that at 0 terrestrial days, the temperature is approximately -77 degrees celsius. If we look at the next point where the temperature goes through an entire cycle (meaning a high point of around -63 degrees celsius and a low point of around -87 degrees celsius) and reaches -77 degrees celsius, the next number for terrestrial days is approximately 700 terrestrial days.
    We can also use the peaks to estimate the number of terrestrial days in a martian year. Looking at the highest peaks around 850 terrestrial days and 1500 days, we see a difference of around 700 days. 
    According to NASA Science, Mars completes a rotation every 24.6 hours and a year on Mars lasts approximately 669.6 sols (short for solar days). 
    Based on this logic, one rotation for Earth is 23.9 hours. The math is simple, 24.6 hours/23.9 hours * 669.6 sols. This gives us approximately 689 days for Earth. This is very close to the provided number on Nasa Science's site of 687 days. 
    My visual estimate of around 700 terrestrial days is very close to the 687 terrestrial days provided by Nasa Science. (reference link : https://science.nasa.gov/mars/facts/)
6.Export the DataFrame to a CSV file.
The CSV file is labeled 'mars_weather_analysis.csv'.
