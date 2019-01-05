# Web-Scraping
A technique employed to extract large amounts of data from websites whereby the data is extracted and saved to a local file in the computer or to a database in table (spreadsheet) format

Web scraping of http://www.fallingrain.com/world/IN/ is done in this code.

I have mainly used Request and BeatuifulSoup Library for implementing the code.The Requests library allows us to make use of HTTP within our Python programs in a human readable way, and the Beautiful Soup module is designed to get web scraping done quickly.

Links at multiple level changes by single character.
For Example : 
Cities in Rajasthan, starting with 'J' has link : http://www.fallingrain.com/world/IN/24/a/J/
and starting with 'Ja' has link : http://www.fallingrain.com/world/IN/24/a/J/a/
Thus we add characters to the link, to get onto next-level.


We generate links and then check whether the given link or url is valid or not.

If the url is active, then we need to see whether the given webpage contains the required data in the form of 'City', 'Latitude', etc. or the links leading to next level. 

If webpage contains required data, then the data is added to the Pandas Dataframe. 

If it contain only links to the next-level, then we generate next-level url.

Lastly dataframe is exported to CSV 
